# Amazon WorkSpaces Language and Keyboard Support<a name="language_keyboard"></a>

To use the same language and keyboard settings on your client device and your WorkSpace, use one of the following methods, depending on which protocol your WorkSpace is using: PCoIP or WorkSpaces Streaming Protocol \(WSP\)\. 

**Note**  
The following procedures might require you to sign out of Windows or disconnect from your WorkSpace\. Be sure to save your work before proceeding\.

## WorkSpaces Using the PCoIP Protocol<a name="lang-keyboard-pcoip"></a>

If you're using a language\-specific keyboard, use one of the following methods to make your keyboard and your WorkSpace language settings match\.
+ **Method 1** — Change the keyboard and language settings on your device so that they match the language of your WorkSpace\.
+ **Method 2** — If you are in an AWS Region that supports more than one language, have your WorkSpaces administrator create a WorkSpace for you in your preferred language\. Windows WorkSpaces are currently available in all Regions in English \(US\)\. 

  In certain Regions, other languages are available\. In the Canada \(Central\) Region, Windows WorkSpaces are also available in French \(Canadian\); in the Asia Pacific \(Seoul\) Region, Korean is also available; in the Asia Pacific \(Tokyo\) Region, Japanese is also available; and in the China \(Ningxia\) Region, Chinese \(Simplified\) is also available\.

  To see which Region your WorkSpace is in, log in to the WorkSpaces client application, and then choose **Support**, **About My WorkSpace**\.
+ **Method 3** — Install the appropriate language or keyboard settings on your WorkSpace\. For a Windows WorkSpace, use the following steps:

  1. Log in to the WorkSpace\.

  1. On the Windows **Start** menu, choose **Settings**\.

  1. Choose **Time & Language**, and then choose **Language**\.

  1. Under **Preferred languages**, choose **Add a language**\.

  1. In the **Choose a language to install** dialog box, select the language to add, and then choose **Next**\.

  1. In the **Install language features** dialog box, select the language features that you want, and then choose **Install**\. For example, if you only want to add support for a language\-specific keyboard, select **Basic typing** to install keyboard support for that language\.

  1. \(Optional\) If you've chosen a new display language, sign out of Windows and then sign back in to see the changes take effect\.

  1. If you didn't change the display language, select the new keyboard layout for the language that you installed\. To do so, in the Windows taskbar, choose **ENG** in the lower\-right corner next to the date and time\. A menu appears\. Select the language keyboard that you want to use for input\.

## WorkSpaces Using the WorkSpaces Streaming Protocol \(WSP\)<a name="lang-keyboard-wsp"></a>

The following languages require the use of an Input Method Editor \(IME\) to enter characters that aren't found on a QWERTY keyboard:
+ Amharic \(Ethiopia\)
+ Chinese \(PRC\)
+ Chinese \(Traditional\)
+ Chinese \(Traditional DaYi input method\)
+ Chinese \(Wubi input method\)
+ Chinese \(Yi script\)
+ Japanese \(Japan\)
+ Japanese \(106/109 keyboard layout\)
+ Korean \(Hangul\)
+ Korean \(Old Hangul\)
+ Tigrinya \(Ethiopia\)

If you're using a language\-specific keyboard, you might want your local client device and your remote Windows WorkSpace using the WorkSpaces Streaming Protocol \(WSP\) to automatically use the same keyboard layout\. How you do this depends on whether you're using an IME language or a non\-IME language\. 

**Note**  
If you want to use the Japanese 106/109 keyboard layout, be sure to use the [procedure specific to the Japanese 106/109 layout](#japanese_106_109)\.

**To use a non\-IME language**

If you're using a non\-IME language \(for example, French\), use the following procedure to automatically use the same keyboard layout on your local client device and your remote WorkSpace\.

1. Set the local client device to the language\-specific keyboard that you want\.

   1. On the Windows **Start** menu, choose **Settings**\.

   1. Choose **Time & language**\.

   1. Choose **Language**\.

   1. Under **Preferred languages**, select **Add a language**\.

   1. On the **Choose a language to install** page, select the language you want\.

   1. Choose **Next**\. 

   1. Choose **Install**\. 

   1. If needed, set your language\-specific keyboard layout by selecting the language and then choosing **Options**\. 

   1. \(Optional\) If you chose a new display language, sign out of Windows so that the new display language can take effect\. 

1. Select the new keyboard layout for the language that you installed\. To do so, in the Windows taskbar, choose **ENG** in the lower\-right corner next to the date and time\. A menu appears\. Select the language keyboard that you want to use for input\. 

1. Start your WorkSpaces client application and log into your WSP WorkSpace\.

1. While in your WorkSpace, press any key\. The keyboard layout for your WorkSpace is automatically set to the same one that you chose for your client device\. 

Whenever you start typing in your WSP WorkSpace, the keyboard layout used in your WorkSpace will now automatically be the same as the keyboard layout that's selected on your client device\.

To change the display language in your WorkSpaces desktop client application, see [Client Language \(Linux\)](amazon-workspaces-linux-client.md#linux_client_lang), [Client Language \(macOS\)](amazon-workspaces-osx-client.md#osx_client_lang), or [Client Language \(Windows\)](amazon-workspaces-windows-client.md#windows_client_lang)\.

**To use an IME language other than Japanese 106/109**

If you're using an IME language other than the Japanese 106/109 keyboard layout \(for example, Korean\), use the following procedure to automatically use the same keyboard layout on your local client device and your remote WorkSpace\.

1. Set the local client device's keyboard layout to the IME language that you want\.

   1. On the Windows **Start** menu, choose **Settings**\.

   1. Choose **Time & language**\.

   1. Choose **Language**\.

   1. Under **Preferred languages**, select **Add a language**\.

   1. On the **Choose a language to install** page, select the language that you want\.

   1. Choose **Next**\. 

   1. Choose **Install**\. 

   1. If needed, set your language\-specific keyboard layout by selecting the language and then choosing **Options**\. 

   1. \(Optional\) If you chose a new display language, sign out of Windows so that the new display language can take effect\. 

1. Select the new keyboard layout for the language that you installed\. To do so, in the Windows taskbar, choose **ENG** in the lower\-right corner next to the date and time\. A menu appears\. Select the language keyboard that you want to use for input\. 

1. Start your WorkSpaces client application and log into your WSP WorkSpace\.

1. Inside the WorkSpace, set the input language to the IME language that you want\.

   1. On the Windows **Start** menu, choose **Settings**\.

   1. Choose **Time & language**\.

   1. Choose **Region & language**\.

   1. Under **Languages**, select **Add a language**\.

   1. On the **Add a language** page, select the IME language that you want\.

   1. \(Optional\) If needed, set your language\-specific keyboard layout by selecting the language on the **Language** page and then choosing **Options**\.

   1. \(Optional\) If you chose a new display language, sign out of Windows so that the new display language can take effect\. When you sign out, you're also disconnected from your WorkSpace\.

1. Disconnect from your WorkSpace \(if you didn't already do so in the previous step\)\.

1. Reconnect to your WorkSpace\.

1. Inside the WorkSpace, in the Windows taskbar, choose **ENG** in the lower\-right corner next to the date and time\. A menu appears\. Select the IME language that you installed\. 

You can now use your IME language in your WSP WorkSpace\. Whenever you start typing in your WorkSpace, the keyboard layout used in your WorkSpace will now automatically be the same as the keyboard layout that's selected on your client device\. 

To change the display language in your WorkSpaces desktop client application, see [Client Language \(Linux\)](amazon-workspaces-linux-client.md#linux_client_lang), [Client Language \(macOS\)](amazon-workspaces-osx-client.md#osx_client_lang), or [Client Language \(Windows\)](amazon-workspaces-windows-client.md#windows_client_lang)\.

**To use the Japanese 106/109 keyboard layout**

If you're using the Japanese 106/109 keyboard layout, use the following procedure to automatically use the same keyboard layout on your local client device and your remote WorkSpace\. 

1. Set the local client device’s display language to Japanese, and set the keyboard to use the Japanese 106/109 keyboard layout\. 

   1. On the Windows **Start** menu, choose **Settings**\.

   1. Choose **Time & language**\.

   1. Choose **Language**\.

   1. Under **Preferred languages**, select **Add a language**\.

   1. On the **Choose a language to install** page, select **Japanese**\.

   1. Choose **Next**\. 

   1. On the **Install language features** page, choose **Install**\.

   1. On the **Languages** page, select **Japanese**, and then choose **Options**\.

   1. In the **Language options: Japanese** page, under **Hardware keyboard layout**, choose **Change layout**\.

   1. In the **Change hardware keyboard layout** dialog box, select **Japanese keyboard \(106/109 key\)**\.

   1. The change doesn't take effect until you restart Windows\. Either choose **Restart now**, or choose **OK**, save your work, and then restart Windows\.

1. Select the new keyboard layout that you installed\. To do so, in the Windows taskbar, choose **ENG** in the lower\-right corner next to the date and time\. A menu appears\. Select **Japanese Microsoft IME**\.

1. Start your WorkSpaces client application and log into your WSP WorkSpace\.

1. Inside the WorkSpace, set Japanese as the default display language and set the keyboard layout to Japanese 106/109\.

   1. On the Windows **Start** menu, choose **Settings**\.

   1. Choose **Time & language**\.

   1. Choose **Region & language**\.

   1. Under **Languages**, select **Add a language**\.

   1. On the **Add a language** page, select **Japanese**\.

   1. On the **Languages** page, select **Japanese**, and then choose **Set as default**\.

   1. On the **Languages** page, select **Japanese**, and then choose **Options**\.

   1. In the **Language options** page, under **Hardware keyboard layout**, choose **Change layout**\.

   1. In the **Change hardware keyboard layout** dialog box, select **Japanese keyboard \(106/109 key\)**\.

   1. The change doesn't take effect until you sign out of Windows\. Choose **Sign out**\. 

      You will be signed out of Windows and disconnected from your WorkSpace\.

1. Reconnect to your WorkSpace\.

1. Inside the WorkSpace, in the Windows taskbar, choose **ENG** in the lower\-right corner next to the date and time\. A menu appears\. Select **Japanese Microsoft IME**\. 

You can now use the Japanese 106/109 keyboard layout in your WSP WorkSpace\. Whenever you start typing in your WorkSpace, the keyboard layout used in your WorkSpace will now automatically be the same as the keyboard layout that's selected on your client device\.

To change the display language in your WorkSpaces desktop client application, see [Client Language \(Linux\)](amazon-workspaces-linux-client.md#linux_client_lang), [Client Language \(macOS\)](amazon-workspaces-osx-client.md#osx_client_lang), or [Client Language \(Windows\)](amazon-workspaces-windows-client.md#windows_client_lang)\.