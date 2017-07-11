---
title: "方法 : Windows フォーム DataGridView コントロールのセルと列を、それぞれの動作と外観を拡張してカスタマイズする | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-winforms"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "jsharp"
helpviewer_keywords: 
  - "セル, カスタマイズ (DataGridView コントロール内の)"
  - "列 [Windows フォーム], カスタマイズ (DataGridView コントロール内の)"
  - "DataGridView コントロール [Windows フォーム], セルのカスタマイズ"
ms.assetid: 9b7dc7b6-5ce6-4566-9949-902f74f17a81
caps.latest.revision: 21
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 21
---
# 方法 : Windows フォーム DataGridView コントロールのセルと列を、それぞれの動作と外観を拡張してカスタマイズする
<xref:System.Windows.Forms.DataGridView> コントロールは、プロパティ、イベント、およびコンパニオン クラスを使用して外観と動作をカスタマイズする様々な方法を提供します。  場合によっては、これらの機能が提供するもの以外にも、セルの要件がある場合があります。  独自のカスタム <xref:System.Windows.Forms.DataGridViewCell> クラスを作成して、拡張機能を提供することができます。  
  
 <xref:System.Windows.Forms.DataGridViewCell> 基底クラスまたは派生クラスの 1 つから派生することで、カスタム <xref:System.Windows.Forms.DataGridViewCell> クラスを作成します。  任意の種類の列の任意の種類のセルを表示できますが、多くの場合は、セルの種類の表示に特化したカスタムの <xref:System.Windows.Forms.DataGridViewColumn> クラスを作成することになります。  列のクラスは、<xref:System.Windows.Forms.DataGridViewColumn> または派生型のいずれかから派生します。  
  
 次のコード例では、マウスがセルの境界に入ってでるときを検出する、`DataGridViewRolloverCell` と呼ばれるカスタム セル クラスを作成します。  マウスがセルの範囲内にある場合に、埋め込みの四角形が描画されます。  この新しい型は <xref:System.Windows.Forms.DataGridViewTextBoxCell> から派生して、その他のすべての点では、基底クラスとして動作します。  列のコンパニオン クラスは `DataGridViewRolloverColumn` と呼ばれます。  
  
 これらのクラスを使用するには、<xref:System.Windows.Forms.DataGridView> コントロールを含むフォームを作成して、1 つ以上の `DataGridViewRolloverColumn` オブジェクトを <xref:System.Windows.Forms.DataGridView.Columns%2A> コレクションに追加し、値を含む行にコントロールを設定します。  
  
> [!NOTE]
>  空の行を追加すると、この例は正しく動作しません。  たとえば、<xref:System.Windows.Forms.DataGridView.RowCount%2A> プロパティを設定することでコントロールに行を追加する場合に、空の行を作成します。  これは、この例で追加された行は自動的に共有されるためでです。つまり、`DataGridViewRolloverCell` オブジェクトは、各セルをクリックするまでインスタンス化されないため、関連付けられた行の共有が解除されます。  
  
 この種類のセルのカスタマイズには共有されていない行が必要なため、大量のデータ セットでの使用には適切ではありません。  行の共有の詳細については、「[Windows フォーム DataGridView コントロールを拡張するための推奨される手順](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md)」を参照してください。  
  
> [!NOTE]
>  <xref:System.Windows.Forms.DataGridViewCell> や <xref:System.Windows.Forms.DataGridViewColumn> から派生したクラスに新しいプロパティを追加するときは、`Clone` メソッドをオーバーライドし、複製操作時に新しいプロパティをコピーする必要があります。  また、基底クラスの `Clone` メソッドを呼び出して、基底クラスのプロパティを新しいセルまたは列にコピーする必要もあります。  
  
### DataGridView コントロール内でセルと列をカスタマイズするには  
  
1.  `DataGridViewRolloverCell`という新しいセル クラスを <xref:System.Windows.Forms.DataGridViewTextBoxCell> 型から派生させます。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewRolloverCell#201](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/CS/rollovercell.cs#201)]
     [!code-vb[System.Windows.Forms.DataGridViewRolloverCell#201](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/VB/rollovercell.vb#201)]  
    [!code-csharp[System.Windows.Forms.DataGridViewRolloverCell#202](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/CS/rollovercell.cs#202)]
    [!code-vb[System.Windows.Forms.DataGridViewRolloverCell#202](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/VB/rollovercell.vb#202)]  
  
2.  <xref:System.Windows.Forms.DataGridViewTextBoxCell.Paint%2A> クラスの `DataGridViewRolloverCell` メソッドをオーバーライドします。  オーバーライドで最初にホストされているテキスト ボックスの機能を処理する基本クラスの実装を呼び出します。  次に、コントロールの <xref:System.Windows.Forms.Control.PointToClient%2A> メソッドを使用して、\(画面座標の\) カーソル位置を <xref:System.Windows.Forms.DataGridView> クライアント領域の座標に変換します。  マウスの座標がセルの境界内にある場合は、埋め込みの四角形を描画します。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewRolloverCell#210](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/CS/rollovercell.cs#210)]
     [!code-vb[System.Windows.Forms.DataGridViewRolloverCell#210](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/VB/rollovercell.vb#210)]  
  
3.  `DataGridViewRolloverCell` クラスの <xref:System.Windows.Forms.DataGridViewCell.OnMouseEnter%2A> メソッドと <xref:System.Windows.Forms.DataGridViewCell.OnMouseLeave%2A> メソッドをオーバーライドして、マウス ポインターがに入る時点または出る時点でセルが自身を再描画するよう強制します。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewRolloverCell#220](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/CS/rollovercell.cs#220)]
     [!code-vb[System.Windows.Forms.DataGridViewRolloverCell#220](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/VB/rollovercell.vb#220)]  
  
4.  `DataGridViewRolloverCellColumn` という新しいクラスを <xref:System.Windows.Forms.DataGridViewColumn> 型から派生させます。  コンストラクターで、新しい `DataGridViewRolloverCell` オブジェクトを <xref:System.Windows.Forms.DataGridViewColumn.CellTemplate%2A> プロパティに割り当てます。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewRolloverCell#300](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/CS/rollovercell.cs#300)]
     [!code-vb[System.Windows.Forms.DataGridViewRolloverCell#300](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/VB/rollovercell.vb#300)]  
  
## 使用例  
 完全なコード例には、カスタムのセルの種類の動作を示す小さなテスト フォームが含まれます。  
  
 [!code-csharp[System.Windows.Forms.DataGridViewRolloverCell#000](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/CS/rollovercell.cs#000)]
 [!code-vb[System.Windows.Forms.DataGridViewRolloverCell#000](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewRolloverCell/VB/rollovercell.vb#000)]  
  
## コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Windows.Forms、および System.Drawing の各アセンブリへの参照。  
  
 [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] または [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)] のコマンド ラインからのこの例のビルドについては、「[コマンド ラインからのビルド](../Topic/Building%20from%20the%20Command%20Line%20\(Visual%20Basic\).md)」または「[csc.exe を使用したコマンド ラインからのビルド](../../../../ocs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)」を参照してください。  また、コードを新しいプロジェクトに貼り付けることにより、[!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] でこの例をビルドすることもできます。  「[方法 : 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」も参照してください。  
  
## 参照  
 <xref:System.Windows.Forms.DataGridView>   
 <xref:System.Windows.Forms.DataGridViewCell>   
 <xref:System.Windows.Forms.DataGridViewColumn>   
 [Windows フォーム DataGridView コントロールのカスタマイズ](../../../../docs/framework/winforms/controls/customizing-the-windows-forms-datagridview-control.md)   
 [DataGridView コントロールのアーキテクチャ](../../../../docs/framework/winforms/controls/datagridview-control-architecture-windows-forms.md)   
 [Windows フォーム DataGridView コントロールの列型](../../../../docs/framework/winforms/controls/column-types-in-the-windows-forms-datagridview-control.md)   
 [Windows フォーム DataGridView コントロールを拡張するための推奨される手順](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md)