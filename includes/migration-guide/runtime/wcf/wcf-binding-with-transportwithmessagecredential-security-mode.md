### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>TransportWithMessageCredential セキュリティ モードを使用する WCF バインド

|   |   |
|---|---|
|説明|.NET Framework 4.6.1 より、TransportWithMessageCredential セキュリティ モードを使用する WCF バインドで署名のない非対称のセキュリティ キーの &quot;to&quot; ヘッダーを含むメッセージを取得するように設定できるようになりました。既定では、署名のない &quot;to&quot; ヘッダーは .NET 4.6.1 でも引き続き拒否されます。 これは、アプリケーションが Switch.System.ServiceModel.AllowUnsignedToHeader 構成切り替えを使用するこの新しい動作モードをオプトインした場合にのみ許可されます。これはオプトイン機能であるため、既存のアプリの動作に影響はないはずです。|
|提案される解決策|これはオプトイン機能であるため、既存のアプリの動作に影響はないはずです。 新しい動作を使用するかどうかを制御するには、次の構成設定を使用します。<pre><code>&lt;runtime&gt;<br />&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;<br />&lt;/runtime&gt;</code></pre>|
|スコープ|透明|
|Version|4.6.1|
|型|ランタイム|
|影響を受ける API|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|
