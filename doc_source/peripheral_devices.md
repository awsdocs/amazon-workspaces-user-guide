# WorkSpaces client peripheral device support<a name="peripheral_devices"></a>

The Amazon WorkSpaces client applications offer the following support for peripheral devices\. If you have an issue with using a particular device, have your WorkSpaces administrator send a report to [https://console\.aws\.amazon\.com/support/home\#/](https://console.aws.amazon.com/support/home#/)\.

Device support might differ depending on which streaming protocol your WorkSpace is using, either PCoIP or WorkSpaces Streaming Protocol \(WSP\)\. In the 3\.0\+ versions of the macOS and Windows client applications, you can see which protocol your WorkSpace is using by choosing **Support**, **About My WorkSpace**\. The iPad, Android, and Linux client applications currently support only the PCoIP protocol\.

**Topics**
+ [Monitors](#devices-monitors)
+ [Keyboards and mice](#devices-input)
+ [Audio headsets](#devices-audio)
+ [Printers](#devices-printers)
+ [Scanners, USB drives, and other storage devices](#devices-storage)
+ [Webcams and other video devices](#devices-webcams)
+ [Smart cards](#devices-smart-cards)
+ [Hardware security keys](#hardware-security-keys)

## Monitors<a name="devices-monitors"></a>

The WorkSpaces Android client application supports a single monitor and the use of high DPI displays\. For more information about display support in the WorkSpaces Android client application, see [Display Support for the Android Client](amazon-workspaces-android-client.md#android_display_support)\. For more information about support for high DPI displays, see [WorkSpaces high DPI display support](high_dpi_support.md)\.

The WorkSpaces client applications for Linux, macOS, and Windows support multiple monitors and the use of high DPI displays\.

**Note**  
Multiple monitors aren't currently supported on Linux WorkSpaces using the WorkSpaces Streaming Protocol \(WSP\)\.

For more information about display support in the Linux, macOS, and Windows WorkSpaces client applications, including how to set up multiple monitors, see [Display Support for the Linux Client](amazon-workspaces-linux-client.md#linux-display-support), [Display Support for the macOS Client](amazon-workspaces-osx-client.md#osx-display-support), or [Display Support for the Windows Client](amazon-workspaces-windows-client.md#windows-display-support)\.

For more information about support for high DPI displays, see [WorkSpaces high DPI display support](high_dpi_support.md)\.

## Keyboards and mice<a name="devices-input"></a>

The WorkSpaces client applications for Windows, macOS, and Linux support USB Bluetooth keyboards and mice\.

The WorkSpaces client applications for Android and iPad support touch input, and both clients offer on\-screen keyboards and support keyboards attached to the device\. The Android client supports mice, and [ iPads with iPadOS 13\.4 or later support Bluetooth mice](https://support.apple.com/HT211008)\. The iPad client also supports certain SwiftPoint mice models\. For more information, see [Swiftpoint GT, ProPoint, or PadPoint mouse](amazon-workspaces-ipad-client.md#ipad_gt_mouse)\.

3D mice aren't supported by the WorkSpaces client applications\.

To use languages or keyboards other than English, see [Amazon WorkSpaces language and keyboard support](language_keyboard.md)\. 

## Audio headsets<a name="devices-audio"></a>

Analog and USB audio headsets are supported on the Android, iPad, macOS, Linux, and Windows client applications, and on the PCoIP Zero Client\. We recommend using a headset for audio calls\. If you use your device's built\-in microphone and speakers, you might experience echoing during your conversations\. If you're having difficulty using a headset, see [My headset doesn't work in my WorkSpace](client_troubleshooting.md#headset_problems)\.

**Note**  
Audio currently is not supported on Linux WorkSpaces using the WorkSpaces Streaming Protocol \(WSP\)\.

## Printers<a name="devices-printers"></a>

The Windows and macOS client applications support USB printers and local printing\. The other client applications support other printing methods\. For details about printer support for the various clients, see [Print from a WorkSpace](printing.md)\.

If you're using a PCoIP zero client device to connect to your WorkSpace and you're having trouble using a USB printer or other USB peripheral devices, contact your WorkSpaces administrator for assistance\. For more information, see [ USB printers and other USB peripherals aren't working for PCoIP zero clients](https://docs.aws.amazon.com/workspaces/latest/adminguide/amazon-workspaces-troubleshooting.html#pcoip_zero_client_usb) in the *Amazon WorkSpaces Administration Guide*\.

## Scanners, USB drives, and other storage devices<a name="devices-storage"></a>

The WorkSpaces clients do not support scanners or locally attached peripheral storage devices, such as USB flash drives or external hard drives\.

If you need to transfer, back up, or synchronize files between your WorkSpace and your local client device, consider using [Amazon WorkDocs](workspaces-user-getting-started.md#workdocs-integration) \(if your WorkSpaces administrator has enabled it\)\. You might also be able to email files to yourself\. To see if other solutions are available to you, contact your WorkSpaces administrator\. 

## Webcams and other video devices<a name="devices-webcams"></a>

If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support webcams or other video devices\.

If your WorkSpace is using the WorkSpaces Streaming Protocol \(WSP\), versions 3\.1\.5 and later of the WorkSpaces client applications for Windows and macOS support webcams\. For the Windows client, you must run the client on a machine that's running Windows 10 version 1607 or later\.

**To use a webcam**

1. Log in to your WSP WorkSpace\.

1. Do one of the following, depending on which client you're using\.    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/peripheral_devices.html)

## Smart cards<a name="devices-smart-cards"></a>

If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support smart cards\. 

If your Windows or Linux WorkSpace is using the WSP protocol, version 3\.1\.1 or later of the WorkSpaces client application for Windows and version 3\.1\.5 or later of the WorkSpaces client application for macOS support smart cards\.

For more information about using smart cards with your WorkSpace, see [WorkSpaces client smart card support](smart_card_support.md)\.

## Hardware security keys<a name="hardware-security-keys"></a>

PCoIP Windows WorkSpaces support USB redirection for YubiKey U2F authentication with Windows WorkSpaces client apps\. For more information, see [WorkSpaces USB redirection](usb-redirection.md)\.

### To redirect YubiKey to a WorkSpace for U2F authentication<a name="redirect-yubikey-to-workspace-u2f"></a>
+ To use the YubiKey on your PCoIP WorkSpace, select the **Devices** icon ![\[Devices icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/devices-icon.png) in the upper\-right corner, and then select **Use this device on my remote WorkSpace**\. Choose **Save**\.  
![\[Selection to use on remote WorkSpace\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/device_selection_2.png)
+ To use the YubiKey on your local computer instead of on your WorkSpace, select the ![\[Devices icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/devices-icon.png) in the upper\-right corner, and then select **Use on my local machine**\. Choose **Save**\.  
![\[Selection to use on local machine\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/device_selection_1.png)