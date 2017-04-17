---
title: "&lt;textMessageEncoding&gt; | Microsoft Docs"
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
ms.assetid: e6d834d0-356e-45eb-b530-bbefbb9ec3f0
caps.latest.revision: 14
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 14
---
# &lt;textMessageEncoding&gt;
テキストベースの XML メッセージに使用される文字エンコーディングおよびメッセージ バージョン管理を指定します。  
  
## 構文  
  
```  
  
<textMessageEncoding maxReadPoolSize="Integer"  
   maxWritePoolSize="Integer"  
   messageVersion="Soap11Addressing10/Soap12Addressing10"  
      writeEncoding=”UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding" />  
```  
  
## 属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### 属性  
  
|属性|説明|  
|--------|--------|  
|maxReadPoolSize|新しいリーダーを割り当てずに同時に読み取り可能なメッセージの数を指定する整数です。  プール サイズを大きくすると、システムでは、比較的大きい作業セットで、アクティビティの急増に対する許容度が高まります。  既定値は 64 です。|  
|maxWritePoolSize|新しいライターを割り当てずに同時に送信可能なメッセージの数を指定する整数です。  プール サイズを大きくすると、システムでは、比較的大きい作業セットで、アクティビティの急増に対する許容度が高まります。  既定値は 16 です。|  
|messageVersion|バインディングを使用して送信されたメッセージの SOAP バージョンを指定します。  有効な値は、次のとおりです。<br /><br /> -   Soap11Addressing10<br />-   Soap12Addressing10<br /><br /> 既定値は Soap12Addressing10 です。  この属性は <xref:System.ServiceModel.Channels.MessageVersion> 型です。|  
|writeEncoding|バインドでメッセージの発行に使用される文字セット エンコーディングを指定します。  有効な値は、次のとおりです。<br /><br /> -   UnicodeFffeTextEncoding: Unicode BigEndian エンコーディング<br />-   Utf16TextEncoding: Unicode エンコーディング<br />-   Utf8TextEncoding: 8 ビットのエンコーディング<br /><br /> 既定値は Utf8TextEncoding です。  この属性は <xref:System.Text.Encoding> 型です。|  
  
### 子要素  
  
|要素|説明|  
|--------|--------|  
|[\<readerQuotas\>](../Topic/%3CreaderQuotas%3E.md)|このバインドを使用して設定されるエンドポイントにより処理可能な、SOAP メッセージの複雑さに対する制約を定義します。  この要素は <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 型です。|  
  
### 親要素  
  
|要素|説明|  
|--------|--------|  
|[\<binding\>](../../../../../docs/framework/misc/binding.md)|カスタム バインドのすべてのバインド機能を定義します。|  
  
## 解説  
 エンコーディングは、メッセージをバイト シーケンスに変換するプロセスです。  デコードは、その逆のプロセスです。  WCF \(Windows Communication Foundation\) には、SOAP メッセージのエンコードとして、テキスト、バイナリ、および MTOM \(Message Transmission Optimization Mechanism\) の 3 種類があります。  
  
 `textMessageEncoding` 要素で表されるテキスト エンコーディングでは相互運用性が最も高くなりますが、XML メッセージのエンコーダーとしての効率は最も低くなります。  テキスト エンコーダーは、ネットワーク上でテキストベースのメッセージを作成します。  このエンコーダーにより生成されるメッセージは、WS\-\* ベースの相互運用に適しています。  Web サービスまたは Web サービス クライアントは、一般に、テキスト形式の XML を認識できます。  しかし、大きいブロックのバイナリ データをテキストとして転送するのは、XML メッセージをエンコードする上では、最も非効率的な方法です。  
  
## 使用例  
  
```  
<textMessageEncoding maxReadPoolSize="211"  
    maxWritePoolSize="2132"  
    messageVersion="Soap12Addressing10"  
    textEncoding=”utf-8” />  
```  
  
## 参照  
 <xref:System.ServiceModel.Configuration.TextMessageEncodingElement>   
 <xref:System.ServiceModel.Channels.CustomBinding>   
 <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>   
 <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>   
 [メッセージ エンコーダーを選択する](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)   
 [メッセージ エンコーディング](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)   
 [バインディング](../../../../../docs/framework/wcf/bindings.md)   
 [バインディングの拡張](../../../../../docs/framework/wcf/extending/extending-bindings.md)   
 [カスタム バインディング](../../../../../docs/framework/wcf/extending/custom-bindings.md)   
 [\<customBinding\>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)