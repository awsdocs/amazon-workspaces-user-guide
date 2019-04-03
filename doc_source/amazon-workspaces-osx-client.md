# Amazon WorkSpaces Mac OS X Client Application<a name="amazon-workspaces-osx-client"></a>

The following information will help you get started with the Amazon WorkSpaces Mac OS X client application\.

**Topics**
+ [Requirements](#osx-requirements)
+ [Setup and Installation](#osx_setup)
+ [Connecting to Your WorkSpace](#osx_connecting)
+ [Client Views](#osx_views)
+ [Client Language](#osx_client_lang)
+ [Display Support](#osx-display-support)
+ [Proxy Server](#osx_proxy_server)
+ [Command Shortcuts](#osx_shortcuts)
+ [Release Notes](#osx-release-notes)

## Requirements<a name="osx-requirements"></a>

The client application requires Mac OS X 10\.8\.1 or later\.

## Setup and Installation<a name="osx_setup"></a>

Download and install the Amazon WorkSpaces Mac OS X client from [Amazon WorkSpaces Client Downloads](http://clients.amazonworkspaces.com/)\.

## Connecting to Your WorkSpace<a name="osx_connecting"></a>

To connect to your WorkSpace, complete the following procedure\.

**To connect to your WorkSpace**

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The Amazon WorkSpaces client application uses the registration code and username to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. You can enter a different registration code by launching the client application and choosing **Options**, **Register** in the upper\-left corner on the login screen menu\.

1. Enter your username and password in the login screen and choose **Sign In**\. If your Amazon WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your Amazon WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your Amazon WorkSpaces administrator has not disabled the "Remember Me" feature, you are prompted to save your credentials securely so that you can connect to your WorkSpace easily while the client application remains running\. Your credentials are securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

1. \(Optional\) If your WorkSpace uses an AD Connector directory, you can update the maximum lifetime of the Kerberos ticket by following the steps in [Configuring Kerberos Policies](http://technet.microsoft.com/en-us/library/dd277401.aspx) in the Microsoft TechNet Library\. If you need to disable the "Remember Me" feature, search for help in the [Amazon WorkSpaces forum](https://forums.aws.amazon.com/forum.jspa?forumID=164)\.

An interruption of network connectivity causes an active session to be disconnected\. This can be caused by events such as closing the laptop lid, or the loss of your wireless network connection\. The Amazon WorkSpaces client application for Mac OS X attempts to reconnect the session automatically if network connectivity is regained within a certain amount of time\. The default session resume timeout is 20 minutes, but this timeout may be modified by your network administrator through your domain's Group Policy settings\.

## Client Views<a name="osx_views"></a>

You can switch to full screen mode by choosing **View**, **Show Fullscreen** in the client application menu\.

While in full screen mode, you can switch back to window mode by moving the mouse cursor to the top of the screen\. The client application menu is displayed, and you can choose **View**, **Exit Fullscreen** in the client application menu\.

## Client Language<a name="osx_client_lang"></a>

You can select the language displayed by the client by performing the following steps\.

**Note**  
In the client, Japanese is available in all regions\. However, Japanese is only available in Tokyo for individual WorkSpaces\.

**To select the client language**

1. In the Amazon WorkSpaces client application, open the **Advanced Settings** dialog box\.

1. Enter your desired language in the **Select a language** list and choose **Save**\.

1. Restart the client\.

## Display Support<a name="osx-display-support"></a>

Amazon WorkSpaces supports a maximum of four displays and a maximum resolution of 3840x2160 \(ultra\-high definition, or UHD\)\. The maximum supported resolution depends on the number of displays, as shown in the following table\.


| Displays | Resolution | 
| --- | --- | 
|  2  |  3840x2160  | 
|  4  |  1920x1200  | 

The Amazon WorkSpaces client application extracts the Extended Display Information Data \(EDID\) of all attached displays and determines the best compatibility match before starting the session\. If you have a High DPI display, the client application automatically scales the streaming window according to your local DPI settings\.

## Proxy Server<a name="osx_proxy_server"></a>

If your network requires you to use a proxy server to access the Internet, you can enable the Amazon WorkSpaces client application to use a proxy for HTTPS \(port 443\) traffic\. Proxy with authentication is not currently supported\.

**Note**  
The Amazon WorkSpaces client applications use the HTTPS port for updates, registration, and authentication\. The desktop streaming connections to the WorkSpace require port 4172 to be enabled, and do not go through the proxy server\. 

**To use a proxy server**

1. In the Amazon WorkSpaces client application, open the **Advanced Settings** dialog box\.

1. In the **Proxy Server Setting** area, check **Use Proxy Server**, enter the proxy server address and port, and choose **Save**\.

## Command Shortcuts<a name="osx_shortcuts"></a>

The Amazon WorkSpaces Mac OS X client supports the following command shortcuts:
+ Control\+Option\+Return—Toggle fullscreen display
+ Control\+Option\+F12—Disconnect session

## Release Notes<a name="osx-release-notes"></a>

The following table describes the changes to each release of the client application\.


| Release | Changes | 
| --- | --- | 
|  2\.5\.5  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.2  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.1  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.0  |  Adds support for user self\-service WorkSpace management capabilities  | 
|  2\.4\.10  |  Minor fixes  | 
|  2\.4\.9  |  Minor fixes  | 
|  2\.4\.8  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.7  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.6  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.4  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.2  |  Minor fixes  | 
|  2\.4\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.3\.7  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.3\.6  |  Localization enhancements  | 
|  2\.3\.5  |  Minor improvements  | 
|  2\.3\.3  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.3\.1  |  Minor fixes  | 
|  2\.3\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.2\.3  |  Resolves minor bugs and improves stability  | 
|  2\.2\.1  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.1\.4  |  Resolves a crash issue on macOS Sierra  | 
|  2\.1\.3  |  Closing the client expires the reconnect token\. You can easily reconnect to your WorkSpace as long as the client is running\.  | 
|  2\.1\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.0\.8  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.0\.4  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.1\.80  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.1\.6  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.1\.4  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.0\.8  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.0  |  Initial release  | 