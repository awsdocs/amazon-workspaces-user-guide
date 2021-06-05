# WorkSpaces Client Peripheral Device Support<a name="peripheral_devices"></a>

The Amazon WorkSpaces client applications offer the following support for peripheral devices\. If you have an issue with using a particular device, have your WorkSpaces administrator send a report to [https://console\.aws\.amazon\.com/support/home\#/](https://console.aws.amazon.com/support/home#/)\.

Device support might differ depending on which streaming protocol your WorkSpace is using, either PCoIP or WorkSpaces Streaming Protocol \(WSP\)\. In the 3\.0\+ versions of the macOS and Windows client applications, you can see which protocol your WorkSpace is using by choosing **Support**, **About My WorkSpace**\. The iPad, Android, and Linux client applications currently support only the PCoIP protocol\.

**Note**  
If you're using a PCoIP zero client device to connect to your WorkSpace and you're having trouble using a USB printer or other USB peripheral devices, contact your WorkSpaces administrator for assistance\. For more information, see [ USB printers and other USB peripherals aren't working for PCoIP zero clients](https://docs.aws.amazon.com/workspaces/latest/adminguide/amazon-workspaces-troubleshooting.html#pcoip_zero_client_usb) in the *Amazon Workspaces Administration Guide*\.

**Topics**
+ [Monitors](#devices-monitors)
+ [Keyboards and Mice](#devices-input)
+ [Audio Headsets](#devices-audio)
+ [Printers](#devices-printers)
+ [Scanners, USB Drives, and Other Storage Devices](#devices-storage)
+ [Webcams and Other Video Devices](#devices-webcams)
+ [Smart Cards](#devices-smart-cards)

## Monitors<a name="devices-monitors"></a>

The Workspaces Android client application supports a single monitor and the use of high DPI displays\. For more information about display support in the WorkSpaces Android client application, see [Display Support for the Android Client](amazon-workspaces-android-client.md#android_display_support)\. For more information about support for high DPI displays, see [WorkSpaces High DPI Display Support](high_dpi_support.md)\.

The Workspaces client applications for Linux, macOS, and Windows support multiple monitors and the use of high DPI displays\.

**Note**  
Multiple monitors aren't currently supported on Linux WorkSpaces using the WorkSpaces Streaming Protocol \(WSP\)\.

For more information about display support in the Linux, macOS, and Windows WorkSpaces client applications, including how to set up multiple monitors, see [Display Support for the Linux Client](amazon-workspaces-linux-client.md#linux-display-support), [Display Support for the macOS Client](amazon-workspaces-osx-client.md#osx-display-support), or [Display Support for the Windows Client](amazon-workspaces-windows-client.md#windows-display-support)\.

For more information about support for high DPI displays, see [WorkSpaces High DPI Display Support](high_dpi_support.md)\.

## Keyboards and Mice<a name="devices-input"></a>

The Workspaces client applications for Windows, macOS, and Linux support USB Bluetooth keyboards and mice\.

The WorkSpaces client applications for Android and iPad support touch input, and both clients offer on\-screen keyboards and support keyboards attached to the device\. The Android client supports mice, and [ iPads with iPadOS 13\.4 or later support Bluetooth mice](https://support.apple.com/HT211008)\. The iPad client also supports certain SwiftPoint mice models\. For more information, see [Swiftpoint GT, ProPoint, or PadPoint Mouse](amazon-workspaces-ipad-client.md#ipad_gt_mouse)\.

3D mice aren't supported by the WorkSpaces client applications\.

To use languages or keyboards other than English, see [Amazon Workspaces Language and Keyboard Support](language_keyboard.md)\. 

## Audio Headsets<a name="devices-audio"></a>

Analog and USB audio headsets are supported on the Android, iPad, macOS, Linux, and Windows client applications, and on the PCoIP Zero Client\. We recommend using a headset for audio calls\. If you use your device's built\-in microphone and speakers, you might experience echoing during your conversations\. If you're having difficulty using a headset, see [My headset doesn't work in my WorkSpace](client_troubleshooting.md#headset_problems)\.

**Note**  
Audio currently is not supported on Linux WorkSpaces using the WorkSpaces Streaming Protocol \(WSP\)\.

## Printers<a name="devices-printers"></a>

The Windows and macOS client applications support USB printers and local printing\. The other client applications support other printing methods\. For details about printer support for the various clients, see [Printing from a WorkSpace](printing.md)\.

## Scanners, USB Drives, and Other Storage Devices<a name="devices-storage"></a>

The WorkSpaces clients do not support scanners or locally attached peripheral storage devices, such as USB flash drives or external hard drives\.

If you need to transfer, back up, or synchronize files between your WorkSpace and your local client device, consider using [Amazon WorkDocs](workspaces-user-getting-started.md#workdocs-integration) \(if your WorkSpaces administrator has enabled it\)\. You might also be able to email files to yourself\. To see if other solutions are available to you, contact your WorkSpaces administrator\. 

## Webcams and Other Video Devices<a name="devices-webcams"></a>

If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support webcams or other video devices\.

If your WorkSpace is using the WorkSpaces Streaming Protocol \(WSP\), versions 3\.1\.5 and later of the WorkSpaces client applications for Windows and macOS support webcams\. For the Windows client, you must run the client on a machine that's running Windows 10 version 1607 or later\.

**To use a webcam**

1. Log in to your WSP WorkSpace\.

1. Do one of the following, depending on which client you're using\.    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/peripheral_devices.html)

## Smart Cards<a name="devices-smart-cards"></a>

If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support smart cards\. 

If your Windows or Linux WorkSpace is using the WSP protocol, version 3\.1\.1 or later of the WorkSpaces client application for Windows and version 3\.1\.5 or later of the WorkSpaces client application for macOS support smart cards\.

For more information about using smart cards with your WorkSpace, see [WorkSpaces Client Smart Card Support](smart_card_support.md)\.