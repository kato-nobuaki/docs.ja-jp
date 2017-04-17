---
title: "Visual Studio 用開発者コマンド プロンプト | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "コマンド プロンプト、Windows SDK"
  - "Visual Studio コマンド プロンプト"
  - "コマンド プロンプト、Visual Studio"
  - "SDK のコマンド プロンプト"
  - "ツール [.NET Framework]、環境変数の設定"
  - "環境変数、ツールへの設定"
  - "開発者コマンド プロンプト"
ms.assetid: 94fcf524-9045-4993-bfb2-e2d8bad44219
caps.latest.revision: 45
author: "mairaw"
ms.author: "mairaw"
manager: "wpickett"
caps.handback.revision: 45
---
# Visual Studio 用開発者コマンド プロンプト
Visual Studio の開発者コマンド プロンプトでは、.NET Framework ツールを使いやすくするための環境変数が自動的に設定されます。 開発者コマンド プロンプトは、完全版または Community Edition の Visual Studio でインストールされます。 Express バージョンの Visual Studio ではインストールされません。  
  
<a name="find"></a>   
## コンピューター上でのコマンド プロンプトの検索  
 Visual Studio のバージョンと、インストールした追加の SDK に応じて、複数のコマンド プロンプトが表示される場合があります。 たとえば、Visual Studio の 64 ビット バージョンには、32 ビットと 64 ビットのコマンド プロンプトが用意されています \(ほとんどのツールでは、32 ビット バージョンと 64 ビット バージョンに違いはありませんが、一部のツールでは、32 ビット環境と 64 ビット環境に固有の変更が加えられています\)。 次の手順でうまくいかない場合は、「[コンピューター上のファイルを手動で探す](#alternative)」または「[Visual Studio 内からコマンド プロンプトを実行する](#visualstudio)」を試してください。  
  
 **Windows 10 の場合**  
  
1.  キーボードの Windows ロゴ キー ![Windows のロゴ](../../../docs/framework/install/media/windowskeyboardlogo.png "Windowskeyboardlogo") を押すなどして、**\[スタート\]** メニューを開きます。  
  
2.  **\[スタート\]** メニューで、「`dev`」と入力します。 これにより、検索パターンに一致する、インストールされているアプリの一覧が表示されます。 別のコマンド プロンプトを探す場合は、別の検索語句 \(「`prompt`」など\) を入力してください。  
  
3.  **\[開発者コマンド プロンプト\]** \(または、使用するコマンド プロンプト\) を選択します。  
  
 **Windows 8.1 の場合**  
  
1.  キーボードの Windows ロゴ キー ![Windows のロゴ](../../../docs/framework/install/media/windowskeyboardlogo.png "Windowskeyboardlogo") を押すなどして、**\[スタート\]** 画面に移動します。  
  
2.  **\[スタート\]** 画面で、`CTRL + TAB` キーを押して **\[アプリ\]** 一覧を開き、「`V`」と入力します。 これにより、インストールされているすべての Visual Studio コマンド プロンプトが含まれた一覧が表示されます。  
  
3.  **\[開発者コマンド プロンプト\]** \(または、使用するコマンド プロンプト\) を選択します。  
  
 **Windows 8 の場合**  
  
1.  キーボードの Windows ロゴ キー ![Windows のロゴ](../../../docs/framework/install/media/windowskeyboardlogo.png "Windowskeyboardlogo") を押すなどして、**\[スタート\]** 画面に移動します。  
  
2.  **\[スタート\]** 画面で、Windows ロゴ キー ![Windows のロゴ](../../../docs/framework/install/media/windowskeyboardlogo.png "Windowskeyboardlogo") `+ Z` を押します。  
  
3.  画面下部にある**アプリ ビュー** アイコンを選択し、「`V`」と入力します。 これにより、インストールされているすべての Visual Studio コマンド プロンプトが含まれた一覧が表示されます。  
  
4.  **\[開発者コマンド プロンプト\]** \(または、使用するコマンド プロンプト\) を選択します。  
  
 **Windows 7 の場合**  
  
1.  **\[スタート\]** を選択し、**\[すべてのプログラム\]**、**\[Microsoft Visual Studio\]** の順に展開します。  
  
2.  インストールされている Visual Studio のバージョンに応じて、**\[Visual Studio ツール\]**、**\[Visual Studio コマンド プロンプト\]**、または使用するコマンド プロンプトを選択します。  
  
 [Windows SDK](http://msdn.microsoft.com/windows/desktop/aa904949) または [Windows Phone SDK](https://dev.windowsphone.com/downloadsdk) をインストールしている場合は、ARM、x86、または x64 の各アーキテクチャ用のコマンド プロンプトがさらに表示される場合があります。 各ツールのドキュメントを参照して、どのバージョンのコマンド プロンプトを使用する必要があるかを確認してください。  
  
<a name="alternative"></a>   
## コンピューター上のファイルを手動で探す  
  インストール済みのコマンド プロンプトのショートカットは、通常 Visual Studio の**\[スタート\] メニュー** 用のフォルダー \(C:\\ProgramData\\Microsoft\\Windows\\Start Menu\\Programs\\Visual Studio 2015\\Visual Studio Tools 内など\) にあります。    ただし、コマンド プロンプトを探しても、何らかの理由によって期待した結果を得られない場合は、そのショートカットを使用するために、コンピューター上でそのショートカットを手動で探すことができます。   VsDevCmd.bat などのコマンド プロンプトのファイル名を検索するか、または Tools フォルダー \(C:\\Program Files \(x86\)\\Microsoft Visual Studio 14.0\\Common7\\Tools など\) に移動します \(パスは、Visual Studio のバージョンとインストール先に応じて変わります\)。  
  
<a name="visualstudio"></a>   
## Visual Studio 内からコマンド プロンプトを実行する  
 簡単にアクセスできるように、Visual Studio の開発者コマンド プロンプトまたは他のコマンド プロンプトを Visual Studio の \[ツール\] メニューに追加することができます。このためには、\[外部ツール一覧\] にそのコマンド プロンプトを追加します。 この追加を行う方法は、次のとおりです。  
  
1.  Visual Studio を開きます。  
  
2.  **\[ツール\]** メニューを選択し、**\[外部ツール...\]** をクリックします。  
  
3.  **\[外部ツール\]** ダイアログ ボックスで、**\[追加\]** ボタンをクリックします。 新しいエントリが表示されます  
  
4.  新しいメニュー項目の **\[タイトル\]** を入力します \(「`コマンド プロンプト`」など\)。  
  
5.  **\[コマンド\]** フィールドに、起動するファイル \(`%comspec%` や `C:\Windows\System32\cmd.exe` など\) を指定します。  
  
6.  **\[引数\]** フィールドに、使用する特定のコマンド プロンプトのある場所を指定します \(`/k "C:\Program Files (x86)\Microsoft Visual Studio 14.0\Common7\Tools\VsDevCmd.bat"` など \(これにより、[!INCLUDE[vs_dev14](../../../includes/vs-dev14-md.md)] でインストールされた開発者コマンド プロンプトが起動されます\)\)。 この値は、Visual Studio のバージョンとインストール先に応じて変更する必要があります。  
  
7.  **\[初期ディレクトリ\]** フィールドの値 \(**\[プロジェクト ディレクトリ\]** など\) を選択します。  
  
8.  **\[OK\]** を選択します。  
  
 この後、新しいメニュー項目が追加され、このコマンド プロンプトに **\[ツール\]** メニューからアクセスできるようになります。  
  
## 参照  
 [ツール](../../../docs/framework/tools/index.md)   
 [Visual Studio の外部ツール](../Topic/Managing%20External%20Tools.md)