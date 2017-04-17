---
title: "&lt;customBinding&gt; | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
ms.assetid: 9da4f960-f64e-4d8a-894d-2b09eba5ce4b
caps.latest.revision: 24
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 24
---
# &lt;customBinding&gt;
ユーザーのメッセージ スタックを完全に制御できます。  
  
## 構文  
  
```  
  
<customBinding>  
    <binding name="string"  
        closeTimeout="TimeSpan"  
        openTimeout="TimeSpan"   
        receiveTimeout="TimeSpan"  
        sendTimeout="TimeSpan"  
       <compositeDuplex clientBaseAddress="Uri"/>  
       <reliableSession acknowledgementInterval="TimeSpan"  
           advancedFlowControl="Boolean"   
           bufferedMessagesQuota="Integer"  
           inactivityTimeout="TimeSpan"  
           maxPendingChannels="Integer"  
           maxRetryCount="Integer"   
           ordered="Boolean" />  
       <pnrpPeerResolver />  
       <windowsStreamSecurity protectionLevel="None/Sign/EncryptAndSign"/>  
       <sslStreamSecurity requireClientCertificate="Boolean" />  
              <transactionFlow transactionProtocol="OleTransactions/WSAtomicTransactionOctober2004"/>  
       <security   
          defaultAlgorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
           authenticationMode="UserNameForAnonymous"  
           contextMode="Cookie"   
           defaultProtectionLevel="Sign"  
           enableKeyDerivation="false"  
           keyEntropyMode="ClientEntropy"   
                  messageProtectionOrder="SignBeforeEncryptAndEncryptSignature"   
           securityVersion="WSSecurityXXX2005">  
           <localClientSettings cacheCookies="false"  
               detectReplays="false"  
               maxCookieCachingTime="00:07:24" />  
           <localServiceSettings replayCacheSize="9"  
               maxClockSkew="00:00:03"   
               replayWindow="00:07:22.2190000" />  
       </security>  
       <binaryMessageEncoding maxReadPoolSize="Integer"  
           maxWritePoolSize="Integer"  
           maxSessionSize="Integer" />  
       <httpsTransport manualAddressing="Boolean"  
           maxMessageSize="Integer"  
           authenticationScheme="Negotiate"   
           bypassProxyOnLocal="Boolean"  
           hostNameComparisonMode="Exact"   
           mapAddressingHeadersToHttpHeaders="Boolean"   
           proxyaddress="Uri"  
           realm="String"   
           requireClientCertificate="Boolean" />  
       <peerTransport manualAddressing="false"  
          maxMessageSize="20002"  
          listenIPAddress="202.10.1.9"   
          messageAuthentication="false"  
          peerNodeAuthenticationMode="None"  
          port="1000" />  
  
<security   
      defaultAlgorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
   authenticationMode="UserNameForAnonymous"  
   bootstrapBindingConfiguration="String"  
   bootstrapBindingSectionName="String"  
   defaultProtectionLevel="None/Sign/EncryptAndSign"  
      requireDerivedKeys="Boolean"  
   securityHeaderLayout="Strict/Lax/LaxTimestampFirst/LaxTimestampLast"  
   includeTimestamp="Boolean"  
   keyEntropyMode="ClientEntropy/ServerEntropy/CombinedEntropy"   
   messageProtectionOrder="SignBeforeEncrypt/SignBeforeEncryptAndEncryptSignature/EncryptBeforeSign"   
   protectTokens="Boolean"  
   requireSecurityContextCancellation="Boolean"  
   securityVersion=" WSSecurityJan2004/WSSecurityXXX2005"  
   requireSignatureConfirmation="Boolean" >  
   <localClientSettings cacheCookies="Boolean"  
      detectReplays="Boolean"  
      replayCacheSize="Integer"  
      maxClockSkew="TimeSpan"  
      maxCookieCachingTime="TimeSpan"  
      replayWindow="TimeSpan"  
      sessionKeyRenewalInterval="TimeSpan"  
      sessionKeyRolloverInterval="TimeSpan"  
      reconnectOnTransportFailure="Boolean"  
      timestampValidityDuration="TimeSpan"  
      cookieRenewalThresholdPercentage="Integer" />  
   <localServiceSettings detectReplays="Boolean"  
      issuedCookieLifeTime="TimeSpan"  
      maxStatefulNegotiations="Integer"  
            replayCacheSize="Integer"  
      maxClockSkew="TimeSpan"   
      negotiationTimeout="TimeSpan"  
      replayWindow="TimeSpan"  
      inactivityTimeout="TimeSpan"  
      sessionKeyRenewalInterval="TimeSpan"  
      sessionKeyRolloverInterval="TimeSpan"  
      reconnectOnTransportFailure="Boolean"  
      maxConcurrentSessions="Integer"  
      timestampValidityDuration="TimeSpan" />  
   <federationParameters trustVersion="WSTrustApr2004/WSTrustFeb2005" />  
<security   
   defaultAlgorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/ Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
   authenticationMode="UserNameForAnonymous"  
   bootstrapBindingConfiguration="String"  
   bootstrapBindingSectionName="String"  
   defaultProtectionLevel="None/Sign/EncryptAndSign"  
      requireDerivedKeys="Boolean"  
   securityHeaderLayout="Strict/Lax/LaxTimestampFirst/LaxTimestampLast"  
   includeTimestamp="Boolean"  
   keyEntropyMode="ClientEntropy/ServerEntropy/CombinedEntropy"   
   messageProtectionOrder="SignBeforeEncrypt/SignBeforeEncryptAndEncryptSignature/EncryptBeforeSign"   
   protectTokens="Boolean"  
   requireSecurityContextCancellation="Boolean"  
   securityVersion=" WSSecurityJan2004/WSSecurityXXX2005"  
   requireSignatureConfirmation="Boolean" >  
   <localClientSettings cacheCookies="Boolean"  
      detectReplays="Boolean"  
      replayCacheSize="Integer"  
      maxClockSkew="TimeSpan"  
      maxCookieCachingTime="TimeSpan"  
      replayWindow="TimeSpan"  
      sessionKeyRenewalInterval="TimeSpan"  
      sessionKeyRolloverInterval="TimeSpan"  
      reconnectOnTransportFailure="Boolean"  
      timestampValidityDuration="TimeSpan"  
      cookieRenewalThresholdPercentage="Integer" />  
   <localServiceSettings detectReplays="Boolean"  
      issuedCookieLifeTime="TimeSpan"  
      maxStatefulNegotiations="Integer"  
            replayCacheSize="Integer"  
      maxClockSkew="TimeSpan"   
      negotiationTimeout="TimeSpan"  
      replayWindow="TimeSpan"  
      inactivityTimeout="TimeSpan"  
      sessionKeyRenewalInterval="TimeSpan"  
      sessionKeyRolloverInterval="TimeSpan"  
      reconnectOnTransportFailure="Boolean"  
      maxConcurrentSessions="Integer"  
      timestampValidityDuration="TimeSpan" />  
   <federationParameters trustVersion="WSTrustApr2004/WSTrustFeb2005" />  
   <GenericIssuedTokenParameters>   
      <LocalIssuerIssuedTokenParameters keyType=" SymmeticKey/PublicKey"  
        keySize="Integer"  
        tokenType="String" />  
     <IssuedTokenParametersEndpointAddress address="URI"  
        bindingConfiguration="String"  
        binding="String" />  
     <IssuedTokenClient localIssuerChannelBehaviors="String"  
        cacheIssuedTokens="Boolean"  
        maxIssuedTokenCachingTime="TimeSpan"  
        keyEntropyMode="ClientEntropy/ServerEntropy/CombinedEntropy" />  
     <IssuedTokenClientBehavior issuerAddress="String"  
        behaviorConfiguration="String" />  
     <IssuedTokenClientBehavior address="URI"  
        bindingConfiguration="String"  
        binding="String" />  
   </GenericIssuedTokenParameters>   
</security>  
</binding>  
</customBinding>  
```  
  
## 属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### 属性  
  
|属性|説明|  
|--------|--------|  
|closeTimeout|クローズ操作が完了するまでの期間を指定する <xref:System.TimeSpan> 値。  この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。  既定値は 00:01:00 です。|  
|name|バインディングの構成名を格納する文字列です。  この値は、カスタム バインディングの識別文字列として機能するユーザー定義文字列です。  [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] 以降では、バインディングおよび動作に名前を付ける必要はありません。  既定の構成、および名前のないバインディングと動作の詳細については、「[簡略化された構成](../../../../../docs/framework/wcf/simplified-configuration.md)」および「[WCF サービスの簡略化された構成](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)」を参照してください。|  
|openTimeout|実行中の操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。  この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。  既定値は 00:01:00 です。|  
|receiveTimeout|受信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。  この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。  既定値は 00:01:00 です。|  
|sendTimeout|送信操作が完了するまでの時間間隔を指定する <xref:System.TimeSpan> 値です。  この値は必ず <xref:System.TimeSpan.Zero> 以上である必要があります。  既定値は 00:01:00 です。|  
  
### 子要素  
  
|要素|説明|  
|--------|--------|  
|[\<compositeDuplex\>](../../../../../docs/framework/configure-apps/file-schema/wcf/compositeduplex.md)|カスタム バインディングの双方向のメッセージングを指定します。  たとえば HTTP のように、ネイティブでの二重通信を許可しないトランスポートで使用されます。  これとは対照的に、TCP では、二重通信がネイティブで許可されているので、クライアントにメッセージを返信するためにこのバインディング要素をサービスで使用する必要はありません。<br /><br /> クライアントは、サービスのアドレスを公開して、アクセスおよび接続の確立ができるようにする必要があります。  このクライアント アドレスは、`ClientBaseAddress` 属性によって提供されます。<br /><br /> この要素は <xref:System.ServiceModel.Configuration.CompositeDuplexElement> 型です。|  
|[\<pnrpPeerResolver\>](../../../../../docs/framework/configure-apps/file-schema/wcf/pnrppeerresolver.md)|PNRP \(Peer Name Resolution Protocol\) ピア名リゾルバーを指定します。  この要素は <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement> 型です。|  
|[\<reliableSession\>](../../../../../docs/framework/configure-apps/file-schema/wcf/reliablesession.md)|WS\-ReliableMessaging の設定を指定します。  この要素がカスタム バインディングに追加される場合、その結果となるチャネルにより、正確に 1 回の配信保証をサポートできます。  この要素は <xref:System.ServiceModel.Configuration.ReliableSessionElement> 型です。|  
|[\<security\>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md)|カスタム バインディングのセキュリティ オプションを指定します。  この要素は <xref:System.ServiceModel.Configuration.SecurityElement> 型です。|  
|[\<sslStreamSecurity\>](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md)|SSL ストリーム バインディングのセキュリティ設定を指定します。  この要素は <xref:System.ServiceModel.Configuration.SslStreamSecurityElement> 型です。|  
|[\<transactionFlow\>](../../../../../docs/framework/configure-apps/file-schema/wcf/transactionflow.md)|バインディングがトランザクション フローをサポートし、プロトコルが `transactionProtocol` 属性によって使用される必要があることを指定します。  この要素は <xref:System.ServiceModel.Configuration.TransactionFlowElement> 型です。|  
|[\<windowsStreamSecurity\>](../../../../../docs/framework/configure-apps/file-schema/wcf/windowsstreamsecurity.md)|カスタム バインディングのストリーミング セキュリティのオプションを指定します。  この要素は <xref:System.ServiceModel.Configuration.WindowsStreamSecurityElement> 型です。|  
  
### 親要素  
  
|要素|説明|  
|--------|--------|  
|バインディング|Windows Communication Foundation アプリケーションのすべてのバインディングを含みます。|  
  
## 解説  
 カスタム バインディングを使用すると、WCF メッセージ スタックのフル コントロールが可能になります。  特定のエンティティの構成要素を追加した、特別にカスタマイズされたバインディングを作成できます。  たとえば、ユーザーは `httpsTransport` セクション、`reliableSession` セクション、および `security` セクションを組み合わせて、信頼できるセキュリティで保護された HTTPS ベースのバインディングを作成できます。  
  
 個別のバインディングは、メッセージ スタックを、スタック要素の構成要素をスタックに出現する順序で指定することにより定義します。  各要素は、スタック内の 1 つの要素を定義および構成します。  各カスタム バインディング内のトランスポート要素は 1 つだけにする必要があります。  この要素がない場合、メッセージ スタックは不完全です。  
  
 要素がスタックに出現する順序は重要です。それは、その順序で操作がメッセージに適用されるためです。  スタック要素で推奨される順序を次に示します。  
  
1.  トランザクション \(省略可能\)  
  
2.  リライアブル メッセージ機能 \(省略可能\)  
  
3.  セキュリティ \(省略可能\)  
  
4.  Transport  
  
5.  エンコーダー \(省略可能\)  
  
 システムが提供するバインディングの中にサービスの要件を満たすものがない場合は、カスタム バインディングを使用します。  たとえば、カスタム バインドを使用すると、サービス エンドポイントで新しいトランスポートや新しいエンコーダーを使用できます。  
  
 カスタム バインドは、特定の順序で "積み重ねられている" バインド要素のコレクションから <xref:System.ServiceModel.Channels.CustomBinding.%23ctor%2A> の 1 つを使用して作成します。  
  
-   最上位にあるのは、トランザクションのフローを可能にするオプションの <xref:System.ServiceModel.Channels.TransactionFlowBindingElement> です。  
  
-   その次にあるのは、WS\-ReliableMessaging 仕様で定義されているセッションおよび順序指定のメカニズムを提供するオプションの <xref:System.ServiceModel.Channels.ReliableSessionBindingElement> です。  このセッションの概念は、SOAP およびトランスポート中継局を通過できます。  
  
-   その次にあるのは、承認、認証、保護、機密性などのセキュリティ機能を提供するオプションのセキュリティ バインド要素です。  [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] では、次のセキュリティ バインド要素が提供されています。  
  
    -   <xref:System.ServiceModel.Channels.SecurityBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.TransportSecurityBindingElement>  
  
-   その次にあるのは、バインド要素によって指定されるオプションのメッセージ パターンです。  
  
-   <xref:System.ServiceModel.Channels.CompositeDuplexBindingElement>  
  
-   その次にあるのは、オプションのトランスポート アップグレード\/ヘルパー バインド要素です。  
  
    -   <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.WindowsStreamSecurityBindingElement>  
  
-   その次にあるのは、必須のメッセージ エンコード バインディング要素です。  独自のトランスポートを使用することも、以下のメッセージ エンコード バインドのいずれかを使用することもできます。  
  
    -   <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement>  
  
-   最下位には、必須のトランスポート要素があります。  独自のトランスポートを使用することも、[!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] で提供されるトランスポート バインド要素のいずれかを使用することもできます。  
  
    -   <xref:System.ServiceModel.Channels.TcpTransportBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.HttpTransportBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.HttpsTransportBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>  
  
    -   <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBindingElement>  
  
    -   <xref:System.ServiceModel.Channels.PeerTransportBindingElement>  
  
 各層のオプションの概要を次の表に示します。  
  
|レイヤー|オプション|必須|  
|----------|-----------|--------|  
|トランザクション フロー|<xref:System.ServiceModel.Channels.TransactionFlowBindingElement>|Ｘ|  
|信頼性|<xref:System.ServiceModel.Channels.ReliableSessionBindingElement>|Ｘ|  
|セキュリティ|同期、非同期、トランスポート レベル|Ｘ|  
|形状の変更|<xref:System.ServiceModel.Channels.CompositeDuplexBindingElement>|Ｘ|  
|トランスポートのアップグレード|SSL ストリーム、Windows ストリーム、ピア リゾルバー|Ｘ|  
|エンコーディング|テキスト、バイナリ、MTOM、カスタム|はい|  
|Transport|TCP、名前付きパイプ、HTTP、HTTPS、MSMQ のフレーバー、カスタム|はい|  
  
 さらに、独自のバインド要素を定義し、それを定義済みの層のいずれかの間に挿入できます。  
  
 カスタム バインディングを使用してシステム提供のバインディングを変更する方法については、「[方法 : システム指定のバインディングをカスタマイズする](../../../../../docs/framework/wcf/extending/how-to-customize-a-system-provided-binding.md)」を参照してください。  
  
## 参照  
 <xref:System.ServiceModel.Channels.Binding>   
 <xref:System.ServiceModel.Channels.BindingElement>   
 <xref:System.ServiceModel.Configuration.BindingsSection>   
 <xref:System.ServiceModel.Channels.CustomBinding>   
 [\<binding\>](../../../../../docs/framework/misc/binding.md)   
 [バインディング](../../../../../docs/framework/wcf/bindings.md)   
 [バインディングの拡張](../../../../../docs/framework/wcf/extending/extending-bindings.md)   
 [カスタム バインディング](../../../../../docs/framework/wcf/extending/custom-bindings.md)   
 [customBinding Element](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)   
 [バインディング](../../../../../docs/framework/wcf/bindings.md)   
 [システムが提供するバインディングの構成](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)   
 [Using Bindings to Configure Windows Communication Foundation Services and Clients](http://msdn.microsoft.com/ja-jp/bd8b277b-932f-472f-a42a-b02bb5257dfb)