---
title: "同時実行 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "同時実行のサンプル [Windows Communication Foundation]"
  - "サービスの動作, 同時実行のサンプル"
ms.assetid: f8dbdfb3-6858-4f95-abe3-3a1db7878926
caps.latest.revision: 32
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 32
---
# 同時実行
同時実行のサンプルでは、<xref:System.ServiceModel.ServiceBehaviorAttribute> を <xref:System.ServiceModel.ConcurrencyMode> 列挙体と共に使用する方法を示します。この列挙体は、サービスのインスタンスがメッセージを順番に処理するか、または同時に処理するかを制御します。  このサンプルは、`ICalculator` サービス コントラクトを実装する「[概要](../../../../docs/framework/wcf/samples/getting-started-sample.md)」に基づいています。  このサンプルでは、`ICalculator` から継承される新しいコントラクト `ICalculatorConcurrency` を定義します。これによって、サービスの同時実行の状態を検査するための 2 つの操作が追加されます。  同時実行設定を変更してから、クライアントを実行して動作の変更を確認します。  
  
 この例では、クライアントはコンソール アプリケーション \(.exe\) であり、サービスはインターネット インフォメーション サービス \(IIS\) によってホストされます。  
  
> [!NOTE]
>  このサンプルのセットアップ手順とビルド手順については、このトピックの最後を参照してください。  
  
 選択可能な同時実行モードは次の 3 つです。  
  
-   `Single`: 各サービス インスタンスは、一度に 1 つのメッセージを処理します。  これが既定の同時実行モードです。  
  
-   `Multiple`: 各サービス インスタンスは、同時に複数のメッセージを処理します。  この同時実行モードを使用するには、サービスの実装がスレッドセーフである必要があります。  
  
-   `Reentrant`: 各サービス インスタンスは、一度に 1 つのメッセージを処理しますが、再入可能呼び出しを受け入れます。  サービスがこの呼び出しを受け入れるのは、コール アウトするときだけです。  再入は「[ConcurrencyMode.Reentrant](../../../../docs/framework/wcf/samples/concurrencymode-reentrant.md)」サンプルで説明されています。  
  
 同時実行の使用は、インスタンス化モードに関連します。  <xref:System.ServiceModel.InstanceContextMode> インスタンス化では、各メッセージが新しいサービス インスタンスによって処理されるため、同時実行は関係しません。  <xref:System.ServiceModel.InstanceContextMode> インスタンス化では、<xref:System.ServiceModel.ConcurrencyMode> と <xref:System.ServiceModel.ConcurrencyMode> のいずれかの同時実行が関係します。これは 1 つのインスタンスがメッセージを順番に処理するか、同時に処理するかによって決まります。  <xref:System.ServiceModel.InstanceContextMode> インスタンス化では、どの同時実行モードも関係する可能性があります。  
  
 サービス クラスは、`[ServiceBehavior(ConcurrencyMode=<setting>)]` 属性を使用して同時実行動作を指定します。次のサンプル コードを参照してください。  行のコメント化を変更して、`Single` および `Multiple` の同時実行モードをそれぞれ試してみてください。  同時実行モードを変更したら、サービスを再ビルドする必要があります。  
  
```  
// Single allows a single message to be processed sequentially by each service instance.  
//[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single, InstanceContextMode = InstanceContextMode.Single)]  
  
// Multiple allows concurrent processing of multiple messages by a service instance.  
// The service implementation should be thread-safe. This can be used to increase throughput.  
[ServiceBehavior(ConcurrencyMode=ConcurrencyMode.Multiple, InstanceContextMode = InstanceContextMode.Single)]  
  
// Uses Thread.Sleep to vary the execution time of each operation.  
public class CalculatorService : ICalculatorConcurrency  
{  
    int operationCount;  
  
    public double Add(double n1, double n2)  
    {  
        operationCount++;  
        System.Threading.Thread.Sleep(180);  
        return n1 + n2;  
    }  
  
    public double Subtract(double n1, double n2)  
    {  
        operationCount++;  
        System.Threading.Thread.Sleep(100);  
        return n1 - n2;  
    }  
  
    public double Multiply(double n1, double n2)  
    {  
        operationCount++;  
        System.Threading.Thread.Sleep(150);  
        return n1 * n2;  
    }  
  
    public double Divide(double n1, double n2)  
    {  
        operationCount++;  
        System.Threading.Thread.Sleep(120);  
        return n1 / n2;  
    }  
  
    public string GetConcurrencyMode()  
    {     
        // Return the ConcurrencyMode of the service.  
        ServiceHost host = (ServiceHost)OperationContext.Current.Host;  
        ServiceBehaviorAttribute behavior = host.Description.Behaviors.Find<ServiceBehaviorAttribute>();  
        return behavior.ConcurrencyMode.ToString();  
    }  
  
    public int GetOperationCount()  
    {     
        // Return the number of operations.  
        return operationCount;  
    }  
}  
```  
  
 サンプルの既定の設定では、<xref:System.ServiceModel.InstanceContextMode> インスタンス化と <xref:System.ServiceModel.ConcurrencyMode> 同時実行が使用されます。  クライアント コードは、非同期プロキシを使用するように変更されています。  これにより、クライアントはサービスを呼び出した後に、応答を待たずに次の呼び出しを行うことができます。  サービスの同時実行モードの動作の違いを観察してください。  
  
 このサンプルを実行すると、操作要求および応答がクライアントのコンソール ウィンドウに表示されます。  実行中のサービスの同時実行モードが表示され、各操作が呼び出され、その後で操作数が表示されます。  同時実行モードが `Multiple` の場合、結果が返される順序は呼び出された順序とは異なります。サービスは複数のメッセージを同時に実行するからです。  同時実行モードを `Single` に変更すると、結果は呼び出された順序どおりに返されます。サービスは各メッセージを順次処理するからです。  クライアントをシャットダウンするには、クライアント ウィンドウで Enter キーを押します。  
  
### サンプルをセットアップ、ビルド、および実行するには  
  
1.  「[Windows Communication Foundation サンプルの 1 回限りのセットアップの手順](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md)」が実行済みであることを確認します。  
  
2.  Svcutil.exe を使用してプロキシ クライアントを生成する場合は、`/async` オプションを指定します。  
  
3.  ソリューションの C\# 版または Visual Basic .NET 版をビルドするには、「[Windows Communication Foundation サンプルのビルド](../../../../docs/framework/wcf/samples/building-the-samples.md)」の手順に従います。  
  
4.  単一コンピューター構成か複数コンピューター構成かに応じて、「[Windows Communication Foundation サンプルの実行](../../../../docs/framework/wcf/samples/running-the-samples.md)」の手順に従います。  
  
> [!IMPORTANT]
>  サンプルは、既にコンピューターにインストールされている場合があります。  続行する前に、次の \(既定の\) ディレクトリを確認してください。  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  このディレクトリが存在しない場合は、「[.NET Framework 4 向けの Windows Communication Foundation \(WCF\) および Windows Workflow Foundation \(WF\) のサンプル](http://go.microsoft.com/fwlink/?LinkId=150780)」にアクセスして、[!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] および [!INCLUDE[wf1](../../../../includes/wf1-md.md)] のサンプルをすべてダウンロードしてください。  このサンプルは、次のディレクトリに格納されます。  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Behaviors\Concurrency`  
  
## 参照