# WorkSpaces Client Peripheral Device Support<a name="peripheral_devices"></a>


****  

|  | 
| --- |
| Amazon WorkSpaces Streaming Protocol \(WSP\) WorkSpaces are available as a beta service and are subject to change\. WSP beta WorkSpaces should not be used for production workloads\. For more information about the WSP beta, see [Amazon WorkSpaces Streaming Protocol \(beta\)](http://aws.amazon.com/workspaces/wsp/)\. | 

The Amazon WorkSpaces client applications offer the following support for peripheral devices\. If you have an issue with using a particular device, have your WorkSpaces administrator send a report to [https://console\.aws\.amazon\.com/support/home\#/](https://console.aws.amazon.com/support/home#/)\.

**Monitor Support**  
The WorkSpaces client applications for Windows, macOS, and Linux support multiple monitors and the use of high DPI monitors\.

For more information about display support in the WorkSpaces client applications, including how to set up multiple monitors, see [ Display Support for the Linux Client](amazon-workspaces-linux-client.md#linux-display-support), [Display Support for the macOS Client](amazon-workspaces-osx-client.md#osx-display-support), or [Display Support for the Windows Client](amazon-workspaces-windows-client.md#windows-display-support)\.

For more information about support for high DPI monitors, see [WorkSpaces High DPI Display Support](high_dpi_support.md)\.

**USB Bluetooth Keyboards and Mice, USB Audio Headsets, and USB Printers**  
The Amazon WorkSpaces client applications for Windows and macOS support all of these devices\. The WorkSpaces client application for Linux supports USB keyboards and mice\. 

For more information about printing, see [Printing from a WorkSpace](printing.md)\. 

If you're having difficulty using a headset, see [My headset doesn't work in my WorkSpace](client_troubleshooting.md#headset_problems)\.

**Webcams, Other Video Devices, and Storage Devices**  
If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support webcams or other video devices, or other locally attached peripherals such as storage devices\.

If your WorkSpace is using the WorkSpaces Streaming Protocol \(WSP\) beta, the WorkSpaces client applications for Windows and macOS support webcams\.

To use a webcam on your WSP beta WorkSpace, select the **Devices** icon ![\[Devices icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/devices-icon.png) in the upper\-right corner, and then select **Use this device on the remote WorkSpace**\. 

To use a webcam on your local computer instead of on your WorkSpace, select the **Devices** icon ![\[Devices icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/devices-icon.png) in the upper\-right corner, and then select **Use Locally**\. 

**Smart Cards**  
If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support smart cards\. 

If your Linux WorkSpace is using the WSP beta protocol, version 3\.0\.12 or later of the WorkSpaces client application for Windows supports smart cards\.

**Note**  
Both [Common Access Card \(CAC\)](https://www.cac.mil/Common-Access-Card) and [Personal Identity Verification \(PIV\)](https://piv.idmanagement.gov/) smart cards are supported\. Other types of smart cards might also work, but they haven't been fully tested for use with the WSP beta protocol\.
At this time, you can use smart cards only for in\-session authentication, meaning that you can use smart cards only after logging in to your WorkSpace\. You can use smart cards for in\-session authentication for web browsers and applications\. Your WorkSpaces administrator might also have enabled you to run `sudo` or `sudo -i`commands \(if you have administrative privileges on your WorkSpace\)\.
You can use multiple smart cards at the same time for in\-session authentication\.
You can use smart cards only in the AWS GovCloud \(US\-West\) Region\.

To use your smart card with the Chrome browser, use the following procedure\.

1. Log in to your Linux WorkSpace using the WorkSpaces for Windows client application\. 

1. Open Terminal \(**Applications** > **System Tools** > **MATE Terminal**\)\.

1. Run the following command:

   ```
   cd; modutil -dbdir sql:.pki/nssdb/ -add "OpenSC" -libfile /lib64/opensc-pkcs11.so
   ```

1. If Chrome is already running, close it, and then press **Enter**\. When the command finishes running, you should see this message: 

   `Module "OpenSC" added to database.`

You can also use your smart card with the Firefox browser\. Your WorkSpaces administrator might have already enabled Firefox to work with smart cards\. If your smart card doesn't work in Firefox, use the following procedure to enable it\.

1. Open Firefox\. Choose the menu button ![\[Firefox menu button\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/firefox-menu-button.png) in the upper\-right corner, and then choose **Preferences**\. 

1. On the **about:preferences** page, choose **Privacy & Security** in the left navigation pane\.

1. Under **Certificates**, choose **Security Devices**\.

1. In the **Device Manager** dialog box, choose **Load**\. 

1. In the **Load PKCS\#11 Device Driver** dialog box, enter the following:

   **Module Name**: **OpenSC**

   **Module filename**: **/lib64/opensc\-pkcs11\.so**

1. Choose **OK**\. 