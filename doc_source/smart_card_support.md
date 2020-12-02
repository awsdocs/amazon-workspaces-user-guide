# WorkSpaces Client Smart Card Support<a name="smart_card_support"></a>

Version 3\.1\.1 or later of the WorkSpaces Windows client supports smart cards if your Windows or Linux WorkSpace is using the WSP protocol\. If your WorkSpace is using the PCoIP protocol, the WorkSpaces clients do not support smart cards\. 

You can use smart cards for both *pre\-session authentication* and *in\-session authentication*\. Authentication is the process of verifying your identity and confirming that you have access to certain resources\. Pre\-session authentication refers to smart card authentication that's performed while you're logging in to your WorkSpace\. In\-session authentication refers to authentication that's performed during your WorkSpace session, after you log in\. 

For example, you can use smart cards for in\-session authentication while working with web browsers and applications\. You can also use smart cards for performing actions that require administrative permissions\. For example, if you have administrative permissions on your Linux WorkSpace, you can use smart cards to authenticate yourself when running `sudo` and `sudo -i` commands\.

**Note**  
Both [Common Access Card \(CAC\)](https://www.cac.mil/Common-Access-Card) and [Personal Identity Verification \(PIV\)](https://piv.idmanagement.gov/) smart cards are supported\. Other types of smart cards might also work, but they haven't been fully tested for use with the WSP protocol\.
For in\-session authentication and pre\-session authentication on Linux or Windows WorkSpaces, only one smart card is currently allowed at a time\.
Pre\-session authentication is available only in the AWS GovCloud \(US\-West\) Region at this time\. In\-session authentication is available in all Regions where WSP is supported\.
Only the WorkSpaces Windows client application version 3\.1\.1 or later is currently supported for smart card authentication\.
The WorkSpaces Windows client application 3\.1\.1 or later supports smart cards only when the client is running on a 64\-bit version of Windows\.

## Use a Smart Card to Log In to Your WorkSpace<a name="smart-card-login"></a>

**To use your smart card to log in to your WorkSpace**

1. Open version 3\.1\.1 or later of the WorkSpaces Windows client application\.

1. Enter the registration code provided by your WorkSpaces administrator, and then choose **Register**\. You might need to choose **Change Registration Code** at the bottom of the login page so that you can enter a new registration code\.

   After you've entered your registration code, **Insert your smart card** appears on the login page\. If you don't see this text, verify that you've entered the correct registration code\. If you've entered the correct registration code and you don't see this text, contact your WorkSpaces administrator for help\.

1. If you haven't done so already, plug your smart card reader into your local machine, and then insert your smart card into your smart card reader\.

1. On the login page, choose **Insert your smart card**\.

1. The **Certificates** dialog box appears\. Select your certificate, and then choose **OK**\.

1. The **Smart Card** dialog box appears\. Enter your PIN, and then choose **OK**\.

1. On the **Starting WorkSpace** page, enter your PIN again, and then choose **Submit**\.

You should be logged in to your WorkSpace\. If you're unable to sign in, close and reopen the WorkSpaces client application, and then try again\. After trying again, if you still aren't able to sign in, contact your WorkSpaces administrator for help\.

After you have logged in to your WorkSpace, you can continue to use the smart card on your local device as well as in the WorkSpace\.

## Use a Smart Card with Chrome or Firefox on Windows WorkSpaces<a name="smart-card-windows-browsers"></a>

Chrome doesn't require any special configuration to work with your smart card\.

You can also use your smart card with the Firefox browser\. Your WorkSpaces administrator might have already enabled Firefox to work with smart cards\. If your smart card doesn't work in Firefox, contact your WorkSpaces administrator for help\.

## Use a Smart Card with Chrome or Firefox on Linux WorkSpaces<a name="smart-card-linux-browsers"></a>

**To use your smart card with the Chrome browser**

1. Log in to your Linux WorkSpace using the WorkSpaces for Windows client application\. 

1. Open Terminal \(**Applications** > **System Tools** > **MATE Terminal**\)\.

1. Run the following command:

   ```
   cd; modutil -dbdir sql:.pki/nssdb/ -add "OpenSC" -libfile /lib64/opensc-pkcs11.so
   ```

1. If Chrome is already running, close it, and then press **Enter**\. When the command finishes running, you should see this message: 

   `Module "OpenSC" added to database.`

**To use your smart card with the Firefox browser**

Your WorkSpaces administrator might have already enabled Firefox to work with smart cards\. If your smart card doesn't work in Firefox, use the following procedure to enable it\.

1. Open Firefox\. Choose the menu button ![\[Firefox menu button\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/firefox-menu-button.png) in the upper\-right corner, and then choose **Preferences**\. 

1. On the **about:preferences** page, in the left navigation pane, choose **Privacy & Security**\.

1. Under **Certificates**, choose **Security Devices**\.

1. In the **Device Manager** dialog box, choose **Load**\. 

1. In the **Load PKCS\#11 Device Driver** dialog box, enter the following:

   **Module Name**: **OpenSC**

   **Module filename**: **/lib64/opensc\-pkcs11\.so**

1. Choose **OK**\. 