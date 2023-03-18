# WorkSpaces Web Access<a name="amazon-workspaces-web-access"></a>

Users can access their Windows WorkSpaces from any location using a web browser\. This is ideal for users who access WorkSpaces from a personally\-owned or locked\-down device, because installing and maintaining a client application can be challenging\. Instead of using a traditional remote access solution and installing the appropriate client application, users can visit the website to access their work resources\.

**Limits**
+ Web Access is not available for some Windows 10 WorkSpaces that use the PCoIP protocol\. If your PCoIP WorkSpace is powered by Windows Server 2019, Web Access is not available\.
+ You can't use a web browser to connect to GPU\-enabled WorkSpaces or Amazon Linux 2 WorkSpaces. Ubuntu WorkSpaces are supported.
+ As of October 1, 2020, you can't use the Amazon WorkSpaces Web Access client to connect to Windows 7 custom WorkSpaces or to Windows 7 Bring Your Own License \(BYOL\) WorkSpaces\.

**Topics**
+ [Website](#web-access-url)
+ [Requirements](#web-access-requirements)
+ [Client views](#web-access-views)
+ [Proxy servers](#web-access-proxy)

## Website<a name="web-access-url"></a>

Open [WorkSpaces Web Access](https://clients.amazonworkspaces.com/webclient) to log on to your Windows or Ubuntu WorkSpace through your web browser\.

## Requirements<a name="web-access-requirements"></a>

You can access a WorkSpace by running Ubuntu or the Windows 10 desktop experience and one of the following bundles:
+ Value
+ Standard
+ Performance
+ Power
+ PowerPro

You must have web connectivity\.

Your administrator must enable WorkSpaces Web Access\. For more information, see [Enable and Configure Amazon WorkSpaces Web Access](https://docs.aws.amazon.com/workspaces/latest/adminguide/web-access.html) in the *Amazon WorkSpaces Administration Guide*\.

### WorkSpaces configured for PCoIP<a name="workspaces-configured-for-pcoip"></a>

You must run one of the following web browsers on your Windows, macOS, or Linux computer:
+ Google Chrome 55 and later
+ Firefox 52 and later

### WorkSpaces configured for WorkSpaces Streaming Protocol \(WSP\)<a name="workspaces-configured-for-wsp"></a>

You must run one of the following web browsers on your Windows, macOS, or Linux computer:
+ Microsoft Edge 91 and later
+ Google Chrome 91 and later

## Client views<a name="web-access-views"></a>

WorkSpaces Web Access supports multiple screen resolutions\. The minimum supported resolution is 960x720 pixels, and the maximum supported resolution is 2560x1600 pixels\.

Web Access does not support multiple monitors\.

## Proxy servers<a name="web-access-proxy"></a>

If you are required to use a proxy server to access the internet, you can configure your browser to use the proxy server\.

**Limits**
+ Proxy with authentication is not currently supported\.
+ Proxy server support for Web Access can vary by browser\. Chrome \(versions 55 and later\) supports Web Access traffic routed through a web proxy, while the current Firefox does not\.
+ For WorkSpaces configured for WorkSpaces Streaming Protocol \(WSP\), port 4195 \(UDP and TCP\) is used for streaming the WorkSpaces desktop\. Web access does not support the use of a proxy server for port 4195 traffic\. Direct connections are required\. This port must be open to the WSP Gateway IP address ranges\. For more information, see [ WSP gateway servers](https://docs.aws.amazon.com/workspaces/latest/adminguide/workspaces-port-requirements.html#gateway_WSP)\.
