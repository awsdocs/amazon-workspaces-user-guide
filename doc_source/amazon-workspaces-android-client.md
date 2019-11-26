# Amazon WorkSpaces Android Client Application<a name="amazon-workspaces-android-client"></a>

The following information will help you get started with the Amazon WorkSpaces Android client application\.

**Topics**
+ [Requirements](#android-requirements)
+ [Setup and Installation](#android_setup)
+ [Connecting to Your WorkSpace](#android_connecting)
+ [Gestures](#android_gestures)
+ [Radial Menu](#android_radial_menu)
+ [Keyboard](#android_keyboard)
+ [Mouse Modes](#android_mouse_modes)
+ [Disconnect](#android_disconnect)
+ [Release Notes](#android-release-notes)

## Requirements<a name="android-requirements"></a>

The Amazon WorkSpaces Android client application requires the following:
+ Amazon Kindle Fire tablets released after 2012 with Fire OS 4\.0 and later
+ Samsung or Nexus tablets with Android OS 4\.4 and later\. The client application works on most tablets with Android version 4\.4 or later, but some devices might not be compatible\. If you have problems with a device, you can report the problem on the [Amazon WorkSpaces forum](https://forums.aws.amazon.com/forum.jspa?forumID=164)\.

## Setup and Installation<a name="android_setup"></a>

To download and install the client application, complete the following procedure\.

**To download and install the client application**

1. On your tablet, open [https://clients\.amazonworkspaces\.com/](https://clients.amazonworkspaces.com/) and choose the link for your tablet\.

1. Download and install the application\.

1. Verify that the Amazon WorkSpaces client application icon appears on one of the tablet desktops\.

## Connecting to Your WorkSpace<a name="android_connecting"></a>

To connect to your WorkSpace, complete the following procedure\.

**To connect to your WorkSpace**

1. On your tablet, open the Amazon WorkSpaces client application\.

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The Amazon WorkSpaces client application uses the registration code and user name to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. You can enter a different registration code by launching the client application and tapping **Enter new registration code** on the login screen\.

1. Enter your user name and password and tap **Sign In**\. If your Amazon WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your Amazon WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your Amazon WorkSpaces administrator has not disabled the "Remember Me" feature, you are prompted to save your credentials securely so that you can connect to your WorkSpace easily in the future\. Your credentials will be securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

## Gestures<a name="android_gestures"></a>

The following are the gestures that are supported for the Amazon WorkSpaces Android client application\.

Single tap  
Equivalent to a single click in Windows\.

Double tap  
Equivalent to a double click in Windows\.

Two finger single tap  
Equivalent to a right\-click in Windows\.

Two finger double tap  
Toggles the on\-screen keyboard display\.

Swipe from left  
Displays the radial menu\. For more information, see [Radial Menu](#android_radial_menu)

Two finger scroll  
Scrolls vertically\.

Two finger pinch  
Zooms display in or out\.

Two finger pan  
Pans the desktop when zoomed in\.

## Radial Menu<a name="android_radial_menu"></a>

The radial menu is displayed by swiping from the left side of the screen\.

![\[Android radial menu\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial.png)

The radial menu provides quick access to the following features:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-connection-status.png) **Connection Status** – Displays the connection status\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-power.png) **Disconnect** – Disconnects the client application without logging off\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-direct-mouse.png) **Direct Mouse Mode** – Sets the input to direct mouse mode\. For more information, see [Mouse Modes](#android_mouse_modes)\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-help.png) **Help** – Displays the command and gesture tutorial\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-keyboard.png) **Keyboard** – Toggles the display of the on\-screen keyboard\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-windows.png) **Windows Start Menu** – Displays the Windows Start Menu\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-radial-offset-mouse.png) **Offset Mouse Mode** – Sets the input to offset mouse mode\. For more information, see [Mouse Modes](#android_mouse_modes)\. 

## Keyboard<a name="android_keyboard"></a>

To toggle the display of the on\-screen keyboard, double\-tap with two fingers anywhere on the screen\. Special key combinations are displayed in the top row of the keyboard\.

## Mouse Modes<a name="android_mouse_modes"></a>

The mouse mode is set using the [radial menu](#android_radial_menu)\.

### Direct Mode<a name="android_mouse_mode_direct"></a>

In direct mouse mode, the mouse cursor is placed wherever you tap your finger\. In this mode, a single tap is equivalent to a left mouse button click and a two finger single tap is equivalent to a right mouse button click\.

### Offset Mode<a name="android_mouse_mode_offset"></a>

In offset mouse mode, the mouse cursor tracks the movement of your finger on the screen\. In this mode, simulate a left mouse button click by tapping the left mouse button icon\.

![\[Left mouse button icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/mouse-icon-left.png)

Simulate a right mouse button click by tapping the right mouse button icon\.

![\[Right mouse button icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/mouse-icon-right.png)

## Disconnect<a name="android_disconnect"></a>

To disconnect the Android client, display the radial menu, tap the disconnect icon, and tap **Disconnect**\. You can also log off of the WorkSpace, which disconnects the client\.

## Release Notes<a name="android-release-notes"></a>

The following table describes the changes to each release of the Android client application\.


| Release | Changes | 
| --- | --- | 
|  2\.4\.15  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.14  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.13  |  Minor fixes  | 
|  2\.4\.12  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.11  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.10  |  Improves support for Japanese keyboard layouts  | 
|  2\.4\.9  |  Adds support for Samsung Galaxy Note 9  | 
|  2\.4\.7  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.6  |  Adds support for uniform resource identifiers \(URIs\), which enable login orchestration  | 
|  2\.4\.5  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.4  | Minor improvements to session provision handling | 
|  2\.4\.2  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.3\.4  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.3\.3  |  Localization enhancements  | 
|  2\.2\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.1\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.0\.0  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.15  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.11  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.10  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.9  |  Improves the login experience  | 
|  1\.0  |  Initial release  | 