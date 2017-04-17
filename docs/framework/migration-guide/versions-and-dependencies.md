---
title: ".NET Framework のバージョンおよび依存関係 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "バージョン、.NET Framework"
ms.assetid: f75a72de-e2f2-4a7a-9574-3f278684ea90
caps.latest.revision: 122
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
caps.handback.revision: 118
---
# .NET Framework のバージョンおよび依存関係
.NET Framework の各バージョンには、共通言語ランタイム \(CLR\)、基底クラス ライブラリ、およびその他のマネージ ライブラリが含まれています。 このトピックでは、.NET Framework の各バージョンの主要な機能について説明し、基になっている CLR のバージョンおよび関連する開発環境に関する情報と、Windows オペレーティング システムでインストールされる .NET Framework のバージョンを示します。  
  
> [!NOTE]
>  .NET Framework のダウンロードとインストールの詳細については、「[インストール ガイド](../../../docs/framework/install/guide-for-developers.md)」を参照してください。  
  
 次の表に、.NET Framework のバージョン履歴を要約し、各バージョンと Visual Studio、Windows、および Windows Server との関係を示します。 Visual Studio ではマルチターゲット機能が提供されているため、記載されている .NET Framework のバージョンに限定される必要はありません。  
  
 新しい各バージョンの .NET Framework には、1 つ前のバージョンの機能が含まれると共に、新機能が追加されています。 CLR は独自のバージョン番号で識別されます。 .NET Framework のバージョン番号はリリースごとにインクリメントされますが、CLR のバージョンは必ずしもインクリメントされるわけではありません。 たとえば、.NET Framework 4、4.5、およびそれ以降のリリースには CLR 4 が含まれますが、.NET Framework 2.0、3.0、3.5 には CLR 2.0 が含まれます。 \(CLR の Version 3 はありません\)。  
  
 サポートされるオペレーティング システムの全一覧については、「[システム要件](../../../docs/framework/get-started/system-requirements.md)」を参照してください。 ダウンロードについては、「[インストール ガイド](../../../docs/framework/install/guide-for-developers.md)」を参照してください。 コンピューターにインストールされている .NET Framework のバージョンを確認する方法については、「[方法 : インストールされている .NET Framework バージョンを確認する](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照してください。  
  
 次の表では、**\[に含まれる\/Windows 上にインストール可能\]** 列と **\[に含まれる\/Windows Server 上にインストール可能\]** 列に \* のマークが付いているオペレーティング システム バージョンにインストールされる .NET Framework のバージョンは[コントロール パネルで有効にする](../../../docs/framework/install/net-framework-3-5-on-windows-8-plus.md)か \(Windows の場合\)、サーバー マネージャーを利用して有効にする \(Windows Server の場合\) 必要があります。  
  
|.NET Framework のバージョン|CLR バージョン|フィーチャー|Visual Studio バージョンに含まれる|✓ <br /> に含まれる \+ <br />Windows 上にインストール可能|✓ <br /> に含まれる \+ <br />Windows Server 上にインストール可能|インストールされた .NET バージョンを確認するには|  
|---------------------------|---------------|------------|------------------------------|----------------------------------------|-----------------------------------------------|---------------------------------|  
|.NET 4.6.2|4|-   暗号化の機能強化。FIS 186\-3 DSA を含む X509 証明書のサポート、保存されたキーの対称暗号化のサポート、SHA\-2 のハッシュの <xref:System.Security.Cryptography.Xml.SignedXml> サポートが含まれます。また、ECDiffieHellman キー派生ルーチンへの入力がわかりやすくなりました。<br />-   For Windows Presentation Foundation \(WPF\) アプリ、ソフト キーボードのサポート、モニターごとの DPI。<br />-   TLS 1.1 プロトコルと TLS 1.2 プロトコルの ClickOnce サポート。<br />-   Windows フォームおよび WPF アプリの UWP アプリへの変換のサポート。||✓  10 Anniversary Update<br /><br /> \+  10 の 11 月の更新プログラム<br /><br /> \+ 10<br />\+ 8.1<br />\+ 7|\+ 2012 R2<br />\+ 2012<br />\+ 2008 R2 SP1|`Release` DWORD を使用:<br /><br /> -   394802 \(Windows 10 Anniversary Update\)<br />-   394806 \(その他すべての OS バージョン\)<br /><br /> \(「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照\)|  
|Net 4.6.1|4|-   ECDSA を含む X509 証明書のサポート<br />-   ADO.NET のハードウェア保護キーに対する「常に暗号化」のサポート<br />-   WPF におけるスペル チェック機能の向上<br />-   [増やす...](../../../docs/framework/whats-new/index.md)||✓  10 の 11 月の更新プログラム<br /><br /> \+ 10<br />\+ 8.1<br />\+ 8<br />\+ 7|\+ 2012 R2<br />\+ 2012<br />\+ 2008 R2 SP1|`Release` DWORD を使用:<br /><br /> -   394254 \(Windows 10 の 11 月の更新プログラム\)<br />-   394271 \(その他すべての OS バージョン\)<br /><br /> \(「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照\)|  
|.NET 4.6|4|-   .NET ネイティブによるコンパイル<br />-   ASP.NET Core 5.0<br />-   イベント トレーシング機能の強化<br />-   ページのエンコーディングのサポート<br />-   [増やす...](../../../docs/framework/whats-new/index.md)|2015。ただし、一部の .NET ライブラリは、[NuGet](https://www.nuget.org/) から入手できます。 詳細については、「[.NET Framework および特別なリリース](../../../docs/framework/get-started/the-net-framework-and-out-of-band-releases.md)」を参照してください。|✓ 10<br />\+ 8.1<br />\+ 8<br />\+ 7<br />\+ Vista|\+ 2012 R2<br />\+ 2012<br />\+ 2008 R2 SP1<br />\+ 2008 SP2|`Release` DWORD を使用:<br /><br /> -   393295 \(Windows 10\)<br />-   393297 \(その他すべての OS バージョン\)<br /><br /> \(「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照\)|  
|4.5.2|4|-   トランザクション システムと ASP.NET のための新しい API<br />-   Windows フォーム コントロールでのシステム DPI のサイズ変更<br />-   プロファイリングの機能強化<br />-   ETW およびストレス ログの改善<br />-   [増やす...](../../../docs/framework/whats-new/index.md)|\-|\+ 8.1<br />\+ 8<br />\+ 7<br />\+ Vista|\+ 2012 R2<br />\+ 2012<br />\+ 2008 R2 SP1<br />\+ 2008 SP2|`Release` DWORD を使用: 379893<br />\(「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照\)|  
|4.5.1|4|-   Windows Phone ストア アプリのサポート<br />-   自動バインド リダイレクト<br />-   パフォーマンスとデバッグの改善<br />-   [増やす...](../../../docs/framework/whats-new/index.md)|2013|✓ 8.1<br />\+ 8<br />\+ 7<br />\+ Vista|✓ 2012 R2<br />\+ 2012<br />\+ 2008 R2 SP1<br />\+ 2008 SP2|`Release` DWORD を使用:<br /><br /> -   378675 \(Windows 8.1\)<br />-   378758 \(その他\)<br /><br /> \(「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照\)|  
|4.5|4|-   Windows ストア アプリのサポート<br />-   WPF、WCF、WF、ASP.NET の更新<br />-   [増やす...](../../../docs/framework/whats-new/index.md)|2012|✓ 8<br />\+ 7<br />\+ Vista|✓ 2012<br />\+ 2008 R2 SP1<br />\+ 2008 SP2|`Release` DWORD を使用: 378389<br />\(「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照\)|  
|4|4|-   拡張された基底クラス ライブラリ<br />-   ポータブル クラス ライブラリによるクロスプラットフォームでの開発<br />-   MEF、DLR、コード コントラクト<br />-   [増やす...](http://msdn.microsoft.com/library/ms171868\(v=vs.100\).aspx)|2010|\+ 7<br />\+ Vista|\+ 2008 R2 SP1<br />\+ 2008 SP2<br />\+ 2003|「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照|  
|3.5|2.0|-   AJAX 対応の Web サイト<br />-   LINQ<br />-   動的データ<br />-   [増やす...](http://msdn.microsoft.com/library/ms171868\(v=vs.90\).aspx)|2008|✓ 10✓ 8.1\*<br />✓ 8\*<br />✓ 7<br />\+ Vista|✓2008 R2 SP1\*<br />\+ 2012 R2<br />\+ 2012<br />\+ 2008 SP2<br />\+ 2003|「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照|  
|3.0|2.0|-   WPF、WCF、WF、CardSpace|\-|✓ Vista|✓ 2008 R2 SP1\*<br />✓ 2008 SP2\*<br />\+ 2003|「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照|  
|2.0|2.0|-   ジェネリック<br />-   ASP.NET の機能追加<br />-   [増やす...](http://msdn.microsoft.com/library/t357fb32\(v=vs.80\).aspx)|2005|\-|✓ 2008 R2 SP1<br />✓ 2008 SP2<br />✓ 2003|「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照|  
|1.1|1.1|-   ASP.NET と ADO.NET の更新<br />-   side\-by\-side 実行<br />-   [増やす...](http://msdn.microsoft.com/library/9wtde3k4\(v=vs.80\).aspx)|2003|\-|✓ 2003|「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照|  
|1.0|1.0|.NET Framework の最初のバージョン。|Visual Studio .NET|\-|\-|「[手順](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」を参照|  
  
 一般に、コンピューターにインストールされている .NET Framework のバージョンはアンインストールしないでください。使用するアプリケーションが特定のバージョンに依存しており、バージョンが削除されると破損する可能性があるからです。 1 台のコンピューターに複数バージョンの .NET Framework を同時に読み込むことができます。 これは、以前のバージョンをアンインストールすることなく、.NET Framework をインストールできることを意味します。 詳細については、「[作業の開始](../../../docs/framework/get-started/index.md)」を参照してください。  
  
## .NET Framework 4.5 以降のバージョンをターゲットにして実行する  
 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] はコンピューターの [!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)] を置き換えるインプレース更新であり、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)] 4.5.2、4.6、4.6.1、4.6.2 は [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] のインプレース更新です。つまり、同じバージョンのランタイムを使用しますが、アセンブリのバージョンが更新され、新しい型とメンバーが含まれます。 これらの更新プログラムのいずれかをインストールした後、[!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)] アプリ、[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] アプリ、または [!INCLUDE[net_v46](../../../includes/net-v46-md.md)] アプリは再コンパイルせずに実行を継続します。 ただし、逆はできません。 .NET Framework の新しいバージョンをターゲットとするアプリを .NET Framework の以前のバージョンで実行することは推奨されていません。 たとえば、[!INCLUDE[net_v46](../../../includes/net-v46-md.md)] をターゲットとするアプリを [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] で実行することは推奨されていません。 次のガイドラインが適用されます。  
  
-   [!INCLUDE[vs_dev12](../../../includes/vs-dev12-md.md)] では、プロジェクトのターゲット フレームワークとして [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] を選択して \(これにより <xref:Microsoft.Build.Tasks.GetReferenceAssemblyPaths.TargetFrameworkMoniker%2A?displayProperty=fullName> プロパティが設定されます\)、プロジェクトを [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] アセンブリまたは実行可能ファイルとしてコンパイルします。 このアセンブリまたは実行可能ファイルは、[!INCLUDE[net_v45](../../../includes/net-v45-md.md)]、4.5.1、4.5.2、4.6、または 4.6.1 がインストールされているコンピューターで使用できます。  
  
-   Visual Studio で、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)] をプロジェクトのターゲット フレームワークとして選択して \(これにより <xref:Microsoft.Build.Tasks.GetReferenceAssemblyPaths.TargetFrameworkMoniker%2A?displayProperty=fullName> プロパティが設定されます\)、プロジェクトを [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] アセンブリまたは実行可能ファイルとしてコンパイルできます。 このアセンブリまたは実行可能ファイルは [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] かそれ以降のバージョンの .NET Framework がインストールされているコンピューターでのみ実行する必要があります。[!INCLUDE[net_v451](../../../includes/net-v451-md.md)] を対象とする実行可能ファイルは、[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] など、初期バージョンの .NET Framework のみがインストールされたコンピューターでは実行がブロックされ、ユーザーに [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] のインストールを求めるメッセージが表示されます。 また、[!INCLUDE[net_v451](../../../includes/net-v451-md.md)] アセンブリは、[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] など、初期バージョンの .NET Framework を対象とするアプリから呼び出さないでください。  
  
     ここで使用されている [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] と [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] は単なる例にすぎません。 この原則は、実行されているシステムにインストールされているものより新しい .NET Framework のバージョンをターゲットにするアプリに適用されます。  
  
 .NET Framework の変更により、アプリケーション コードの変更が必要な場合があります。既存のアプリケーションを [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] またはそれ以降のバージョンで実行する前に、「[アプリケーションの互換性](../../../docs/framework/migration-guide/application-compatibility.md)」を参照してください。 現行バージョンのインストールの詳細については、「[インストール ガイド](../../../docs/framework/install/guide-for-developers.md)」を参照してください。 .NET Framework のサポートの詳細については、Microsoft サポート Web サイトの「[Microsoft .NET Framework のサポート ライフサイクル ポリシー](http://go.microsoft.com/fwlink/?LinkId=196607)」を参照してください。  
  
## 以前のバージョンのアプリの対象化と実行  
 .NET Framework 2.0、3.0 および 3.5 は、同じバージョンの CLR \(CLR 2.0\) でビルドされています。 これらのバージョンは 1 つのインストールの連続したレイヤーを表します。 各バージョンは、以前のバージョンの上にインクリメンタル方式でビルドされます。 コンピューターでバージョン 2.0、3.0、および 3.5 を side\-by\-side で実行することはできません。 バージョン 3.5 をインストールすると、2.0 と 3.0 のレイヤーが自動的に取得され、バージョン 2.0、3.0、および 3.5 を対象としてビルドされたアプリケーションはすべて、バージョン 3.5 で実行できます。 ただし、.NET Framework 4 でこのレイヤーのアプローチは終了しています。 NET Framework 4 以降では、インプロセスの side\-by\-side ホスティングを使用して、1 つのプロセスで複数のバージョンの CLR を実行できます。 詳細については、「[アセンブリと side\-by\-side 実行](../../../docs/framework/app-domains/assemblies-and-side-by-side-execution.md)」を参照してください。  
  
 さらに、アプリケーションがバージョン 2.0、3.0、または 3.5 を対象とする場合、ユーザーがアプリケーションを実行する前に、[!INCLUDE[win8](../../../includes/win8-md.md)] または [!INCLUDE[win81](../../../includes/win81-md.md)] のコンピューター上で .NET Framework 3.5 を有効にするように求められる場合があります。 詳細については、「[Windows 8 以降のバージョンへの .NET Framework 3.5 のインストール](../../../docs/framework/install/net-framework-3-5-on-windows-8-plus.md)」を参照してください。  
  
## 次の手順  
  
-   .NET Framework での経験がない場合は、[概要](../../../docs/framework/get-started/overview.md)を参照して、主な概念と機能の概要を確認してください。  
  
-   [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] とそのポイント リリースでの新機能と機能強化については、「[新機能](../../../docs/framework/whats-new/index.md)」を参照してください。  
  
-   .NET Framework 4 から [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] およびそのポイント リリースへのアプリの移行に関する詳細については、「[移行ガイド](../Topic/Migration%20Guide%20to%20the%20.NET%20Framework%204.6%20and%204.5%20.md)」を参照してください。  
  
-   コンピューターにどのバージョンまたは更新プログラムがインストールされているかを判別する方法については、「[方法 : インストールされている .NET Framework バージョンを確認する](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)」と「[方法 : インストールされている .NET Framework の更新プログラムを確認する](../../../docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)」を参照してください。  
  
## 参照  
 [バージョンの互換性](../../../docs/framework/migration-guide/version-compatibility.md)   
 [Microsoft .NET Framework のサポート ライフサイクル ポリシー](http://go.microsoft.com/fwlink/?LinkId=196607)   
 [トラブルシューティング](../../../docs/framework/install/troubleshoot-blocked-installations-and-uninstallations.md)