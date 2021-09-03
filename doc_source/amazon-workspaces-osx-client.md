# WorkSpaces macOS client application<a name="amazon-workspaces-osx-client"></a>

The following information helps you get started with the WorkSpaces macOS client application\.

**Topics**
+ [Requirements](#osx-requirements)
+ [Setup and installation](#osx_setup)
+ [Determine your client version](#determine-version-osx)
+ [Connect to your WorkSpace](#osx_connecting)
+ [Manage your login information \(3\.0\+ clients only\)](#manage-login-info-osx)
+ [Client views](#osx_views)
+ [Client language](#osx_client_lang)
+ [Display support](#osx-display-support)
+ [Proxy servers](#osx_proxy_server)
+ [Command shortcuts](#osx_shortcuts)
+ [Remap the Windows logo key or the Command key](#osx_remap_command_key)
+ [Disconnect](#osx_disconnect)
+ [Clipboard support](#osx_clipboard_support)
+ [Release notes](#osx-release-notes)

## Requirements<a name="osx-requirements"></a>

The 3\.0\+ versions of the client application require macOS 10\.12 \(Sierra\) or later\.

The 1\.0\+ or 2\.0\+ versions of the client application require OS X 10\.8\.1 or later\.

**Important**  
**If you use macOS 10\.15 \(Catalina\) or later, you must use version 3\.0\.2 or later of the macOS client\.**  
Versions 2\.5\.11 and earlier of the macOS client can no longer be installed on macOS devices\. These versions also no longer work on devices with macOS Catalina or later\.  
If you are using version 2\.5\.11 or earlier and you upgrade from an older version of macOS to Catalina or later, you will no longer be able to use the 2\.5\.11 or earlier client\. We recommend that affected users upgrade to the latest version of the macOS client that is available for download at [Amazon WorkSpaces Client Downloads](https://clients.amazonworkspaces.com/)\.

**Note**  
If your WorkSpace is located in the Asia Pacific \(Mumbai\) Region, you must use version 3\.1\.3 or later of the Amazon WorkSpaces macOS client application\.

## Setup and installation<a name="osx_setup"></a>

To download and install the client application, complete the following procedure\.

**To download and install the client application**

1. On your macOS device, open [Amazon WorkSpaces Client Downloads](https://clients.amazonworkspaces.com/) and choose the **MacOS X** link\.

1. Download and install the application\.

1. Verify that the Amazon WorkSpaces client application icon appears on the desktop\.

If you're having trouble updating your WorkSpaces macOS client application to a newer version, use the following procedure to update your client application\.

**To update the WorkSpaces macOS client application to a newer version**

1. In the **Finder**, open your **Applications** folder, then open **Utilities**, and choose **Terminal**\.

1. In the Terminal window, enter the following command, and then press the Return key\.

   ```
   defaults delete com.amazon.workspaces SUSkippedVersion
   ```

1. In the Terminal app, choose **Terminal**, **Quit Terminal**\.

1. If you have not already entered a registration code in the WorkSpaces macOS client application, do so, and then choose **Amazon WorkSpaces**, **Quit Amazon WorkSpaces** to close the client application\.

1. Restart the WorkSpaces macOS client application\. You should be prompted to update the client\. Accept the update\.

## Determine your client version<a name="determine-version-osx"></a>

To see which version of the WorkSpaces client you have, choose **Amazon WorkSpaces**, **About Amazon WorkSpaces**, or click the gear icon in the upper\-right corner and choose **About Amazon WorkSpaces**\.

## Connect to your WorkSpace<a name="osx_connecting"></a>

To connect to your WorkSpace, complete the following procedure\.

### To connect to your WorkSpace for 3\.0\+ clients<a name="osx_connecting-new-clients"></a>

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The WorkSpaces client application uses the registration code and user name to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. To enter a different registration code, launch the client application, and then choose **Change Registration Code** at the bottom of the login page\.

1. Enter your user name and password in the login screen and choose **Sign In**\. If your WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your WorkSpaces administrator has not disabled the **Keep me logged in** feature, you can select the **Keep me logged in** check box at the bottom of the login screen to save your credentials securely so that you can connect to your WorkSpace easily while the client application remains running\. Your credentials are securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

### To connect to your WorkSpace for 1\.0\+ and 2\.0\+ clients<a name="osx_connecting-legacy-clients"></a>

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The WorkSpaces client application uses the registration code and user name to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. To enter a different registration code, launch the client application, and then on the menu bar, choose **Options**, **Manage Registrations**\.

1. Enter your user name and password in the login screen and choose **Sign In**\. If your WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your WorkSpaces administrator has not disabled the "Remember Me" feature, you are prompted to save your credentials securely so that you can connect to your WorkSpace easily while the client application remains running\. Your credentials are securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

An interruption of network connectivity causes an active session to be disconnected\. This can be caused by events such as closing the laptop lid, or the loss of your wireless network connection\. The WorkSpaces client application for macOS attempts to reconnect the session automatically if network connectivity is regained within a certain amount of time\. The default session resume timeout is 20 minutes, but this timeout can be modified by your network administrator\.

## Manage your login information \(3\.0\+ clients only\)<a name="manage-login-info-osx"></a>

You can view your registration code and what Region your WorkSpace is in\. You can specify whether you want the WorkSpaces client application to save your current registration code, and you can assign a name to your WorkSpace\. You can also specify if you want Amazon WorkSpaces to keep you logged in to a WorkSpace until you quit or your login period expires\.

**To manage your login information for a WorkSpace**

1. In the WorkSpaces client application, go to **Settings**, **Manage Login Information**\.

1. In the **Manage Login Information** dialog box, you can see the registration code and Region information for your WorkSpace\.

1. \(Optional\) If you want the WorkSpaces client to remember your current registration code, select the **Remember Registration Code** check box\.

1. Under **Saved registration codes**, select the WorkSpace you want to name\.

1. In the **WorkSpace name** box, enter a name for the WorkSpace\.

1. \(Optional\) If you want WorkSpaces to keep you logged in until you quit or your login period expires, select the **Keep me logged in** check box\.

1. Choose **Save**\.

## Client views<a name="osx_views"></a>

You can switch to full screen mode by choosing **View**, **Enter Full Screen** \(3\.0\+ clients\) or **View**, **Show Fullscreen** \(1\.0\+ and 2\.0\+ clients\) in the client application menu\.

While in full screen mode, you can switch back to window mode by moving the pointer to the top of the screen\. The client application menu is displayed, and you can choose **View**, **Leave Full Screen** \(3\.0\+ clients\) or **View**, **Exit Fullscreen** \(1\.0\+ and 2\.0\+ clients\) in the client application menu\.

You can also toggle full screen mode by pressing Control\+Option\+Return\.

## Client language<a name="osx_client_lang"></a>

You can select the language displayed by the client by performing the following steps\.

**Note**  
The WorkSpaces client applications support Japanese\. However, Japanese WorkSpaces are available only in the Asia Pacific \(Tokyo\) Region\.

**To select the client language**

1. Depending on which client you're using, do one of the following\.    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)

1. Enter your desired language in the **Select a language** list and choose **Save**\.

1. Restart the client\.

## Display support<a name="osx-display-support"></a>

WorkSpaces Value, Standard, Performance, Power, PowerPro, and GraphicsPro bundles support a maximum of four displays and a maximum resolution of 3840x2160 \(ultra\-high definition, or UHD\)\. The maximum supported resolution depends on the number of displays, as shown in the following table\.


| Displays | Resolution | 
| --- | --- | 
|  2  |  3840x2160  | 
|  4  |  1920x1200  | 

**Note**  
Graphics bundles support only a single monitor configuration with a maximum resolution of 2560x1600\.

The WorkSpaces client application extracts the Extended Display Information Data \(EDID\) of all attached displays and determines the best compatibility match before starting the session\. If you have a high pixel density \(high DPI\) display, the client application automatically scales the streaming window according to your local DPI settings\. For better maximum resolution with high DPI displays, see [WorkSpaces high DPI display support](high_dpi_support.md)\.

**Note**  
If your screen resolution in WorkSpaces is low and objects look blurry, you need to turn on high DPI mode and adjust the display scaling settings on your Mac\. For more information, see [WorkSpaces high DPI display support](high_dpi_support.md)\.

**To use multiple monitors with WorkSpaces**

1. Configure your local machine to use multiple monitors\. For more information, see [ Use multiple displays with your Mac](https://support.apple.com/guide/mac-help/use-multiple-displays-mchl7c7ebe08/mac) in the Apple documentation\.

1. Start the WorkSpaces client application and log in to your WorkSpace\.

1. Depending on which client you're using, do one of the following:    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)

Your WorkSpace should now be extended across your displays\. Whichever display you have designated as your primary display is also the primary display in WorkSpaces when you enter full screen mode\.

**Note**  
To use full screen mode on only some of the displays in a multiple monitor setup, press and hold the Option key and then click the green maximize button ![\[Maximize button\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/mac-maximize-button.png) in the top\-left corner of the WorkSpaces window\. This button expands the WorkSpaces client window to full size on a screen without extending the WorkSpace to the other displays\. To return to the previous window size, press and hold the Option key and click the maximize button again\.

## Proxy servers<a name="osx_proxy_server"></a>

If your network requires you to use a proxy server to access the internet, you can enable your WorkSpaces client application to use a proxy for HTTPS \(port 443\) traffic\. The WorkSpaces client applications use the HTTPS port for updates, registration, and authentication\. 

**Note**  
The desktop streaming connections to the WorkSpace require ports 4172 and 4195 to be enabled, and do not go through the proxy server\. 
Proxy servers that require authentication with a username and password are not supported\.

### To use a proxy server for 3\.0\+ clients<a name="osx_proxy_server-new-clients"></a>

By default, the 3\.0\+ macOS clients use the proxy server that's specified in the device operating system settings\. The first time the client is launched, the device operating system proxy server setting is used\. If you select another option for the proxy server, that setting is used for subsequent launches of the client\.

**Note**  
If you specify a custom proxy server, a "No network" error might appear when you attempt to log in to your WorkSpace\. To work around this issue, use the default operating system proxy server instead of specifying a custom proxy server in the macOS client\.

1. In the WorkSpaces client application, go to **Settings**, **Manage Proxy Server**\.

1. In the **Set Proxy** dialog box, select **Use proxy server**, enter the proxy server URL or IP address and the port, and choose **Save**\.

### To use a proxy server for 1\.0\+ and 2\.0\+ clients<a name="osx_proxy_server-legacy-clients"></a>

By default, the 1\.0\+ and 2\.0\+ macOS clients don't use a proxy server\. To specify a proxy server, use the following procedure\. 

1. In the WorkSpaces client application, open the **Advanced Settings** dialog box\.

1. In the **Proxy Server Setting** area, select **Use Proxy Server**, enter the proxy server URL or IP address and the port, and choose **Save**\.

## Command shortcuts<a name="osx_shortcuts"></a>

The WorkSpaces macOS client supports the following command shortcuts:


| If you're using\.\.\. | Use these shortcuts | 
| --- | --- | 
|  3\.0\+ client  |  Command\+Q—Quit Amazon WorkSpaces Control\+Option\+Return—Toggle full screen display Control\+Option\+F12—Disconnect session  | 
|  1\.0\+ or 2\.0\+ client  |  Control\+Option\+Return—Toggle full screen display Control\+Option\+F12—Disconnect session  | 

## Remap the Windows logo key or the Command key<a name="osx_remap_command_key"></a>

By default, the Windows logo key on a Windows keyboard and the Command key on an Apple keyboard are both mapped to the Ctrl key when you're using the Amazon WorkSpaces macOS client application\. If you want to change this behavior so that these two keys are mapped to the Windows logo key for use with Windows WorkSpaces, use the following procedure\.

**To map the Windows logo key or the Command key to the Windows logo key**

1. If you haven't already done so, [install or update](#osx_setup) to version 3\.0\.5 or later of the Amazon WorkSpaces macOS client application\.

1. In the **Finder**, open your **Applications** folder, then open **Utilities**, and choose **Terminal**\.

1. In the Terminal window, enter the following command, and then press the Return key\.

   ```
   defaults write "com.amazon.Amazon WorkSpaces Client" remap_cmd_to_ctrl 0
   ```

1. In the Terminal app, choose **Terminal**, **Quit Terminal**\.

1. If your WorkSpaces macOS client application is running, choose **Amazon WorkSpaces**, **Quit Amazon WorkSpaces** in the client to close the client application\.

1. Restart the WorkSpaces macOS client application and log in to your WorkSpace\. The Windows logo key or the Command key should now be mapped to the Windows logo key\.

## Disconnect<a name="osx_disconnect"></a>

To disconnect the macOS client application, you have several options: 
+ In the Amazon WorkSpaces client application, go to **Amazon WorkSpaces**, and then choose **Disconnect WorkSpace**\. Your WorkSpace session ends, but the client application continues running in case you want to log in again\.
+ In the Amazon WorkSpaces client application, go to **Amazon WorkSpaces**, and then choose **Quit Amazon WorkSpaces**\. Your WorkSpace session ends, and the client application closes\.
+ In the Amazon WorkSpaces client application, close the WorkSpaces client window by clicking the red close \(X\) button in the upper\-left corner\. In the **End Session** dialog box, choose **Yes**\. Your WorkSpace session ends, but the client application continues running in case you want to log in again\.
+ You can also log off of the WorkSpace\. In the Amazon WorkSpaces client application, go to **View**, and then choose **Send Ctrl\+Alt\+Delete**\. Choose **Sign Out**\. Your WorkSpace session ends, but the client application continues running in case you want to log in again\.

## Clipboard support<a name="osx_clipboard_support"></a>

The clipboard supports a maximum uncompressed object size of 20 MB\. For more information, see [I'm having trouble copying and pasting](client_troubleshooting.md#copy_paste)\.

**Note**  
When copying from a Microsoft Office app, the clipboard only contains the last copied item, and the item is converted into standard format\. If you copy content larger than 890 KB from a Microsoft Office app, the app might become slow or unresponsive for up to 5 seconds\. 

## Release notes<a name="osx-release-notes"></a>

The following table describes the changes to each release of the client application\.


| Release | Date | Changes | 
| --- | --- | --- | 
| 4\.0\.1 | August 5, 2021 | Minor bug fixes and enhancements\. | 
| 3\.1\.9 | June 29, 2021 | Minor bug fixes and enhancements\. | 
| 3\.1\.8 | May 28, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.1\.7 | April 29, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.1\.6 | April 8, 2021 |  Fixes for disconnects and crashes resulting from WorkSpaces Streaming Protocol \(WSP\) audio traffic optimization  | 
| 3\.1\.5 | April 2, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.1\.4 | March 16, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.1\.3 | February 15, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.1\.2 | January 8, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.1\.0 | December 1, 2020 |  Minor bug fixes and enhancements  | 
| 3\.0\.12 | November 10, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.0\.11 | October 02, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
| 3\.0\.10 | September 16, 2020 |  Adds support for health checks over port 4195 \(UDP and TCP\)  | 
| 3\.0\.9 | August 14, 2020 |  Minor bug fixes and enhancements  | 
| 3\.0\.8 | July 30, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  3\.0\.7  | June 3, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  3\.0\.6  | April 28, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  3\.0\.5  | March 30, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  3\.0\.4  | March 3, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  3\.0\.3  | February 24, 2020 |  Improves readability on high DPI devices  | 
|  3\.0\.2  | February 14, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  3\.0\.0  | November 25, 2019 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.11  | November 4, 2019 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.9  |  |  Minor bug fixes  | 
|  2\.5\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.6  |  |  Minor fixes  | 
|  2\.5\.5  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.2  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.1  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.5\.0  |  |  Adds support for user self\-service WorkSpace management capabilities  | 
|  2\.4\.10  |  |  Minor fixes  | 
|  2\.4\.9  |  |  Minor fixes  | 
|  2\.4\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.6  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.4\.2  |  |  Minor fixes  | 
|  2\.4\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.3\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.3\.6  |  |  Localization enhancements  | 
|  2\.3\.5  |  |  Minor improvements  | 
|  2\.3\.3  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.3\.1  |  |  Minor fixes  | 
|  2\.3\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.2\.3  |  |  Resolves minor bugs and improves stability  | 
|  2\.2\.1  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.1\.4  |  |  Resolves a crash issue on macOS Sierra  | 
|  2\.1\.3  |  |  Closing the client expires the reconnect token\. You can easily reconnect to your WorkSpace as long as the client is running\.  | 
|  2\.1\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.0\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  2\.0\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.1\.80  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.1\.6  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.1\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.0\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-osx-client.html)  | 
|  1\.0  |  |  Initial release  | 