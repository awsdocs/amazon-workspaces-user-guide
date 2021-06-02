# PCoIP Zero Client<a name="amazon-workspaces-pcoip-zero-client"></a>

You can set up and use a PCoIP zero client device with Workspaces\. 

## Requirements<a name="zero_client_reqs"></a>

To use a PCoIP zero client with Workspaces, you need the following:
+ PCoIP zero clients are compatible only with WorkSpaces that are using the PCoIP protocol\.
+ Your Tera2 zero client device must have firmware version 6\.0\.0 or later\. If your Tera2 zero client device has a firmware version between 4\.6\.0 and 6\.0\.0, your Workspaces administrator must upgrade your device firmware through a Desktop Access subscription at [https://www\.teradici\.com/desktop\-access](https://www.teradici.com/desktop-access)\.
+ WorkSpaces multi\-factor authentication \(MFA\) requires a Tera2 zero client device with firmware version 6\.0\.0 or later\.
+ Your WorkSpaces administrator might need to enable your zero client device to use USB printers and other USB peripheral devices\. If you're having trouble using a USB printer or other USB peripheral devices, contact your WorkSpaces administrator for assistance\. For more information, see [ USB printers and other USB peripherals aren't working for PCoIP zero clients](https://docs.aws.amazon.com/workspaces/latest/adminguide/amazon-workspaces-troubleshooting.html#pcoip_zero_client_usb) in the *Amazon Workspaces Administration Guide*\.

For a list of approved PCoIP zero client devices, see [PCoIP Zero Clients](https://www.teradici.com/resource-center/product-service-finder/pcoip-zero-clients) on the Teradici website\.

## Connect to Your WorkSpace<a name="zero_client_connect"></a>

If your zero client device has firmware version 6\.0\.0 or later, you can connect to your WorkSpace\. If your zero client device has a firmware version between 4\.6\.0 and 6\.0\.0, your WorkSpaces administrator must upgrade your device firmware through a Desktop Access subscription at [https://www\.teradici\.com/desktop\-access](https://www.teradici.com/desktop-access)\.

**To connect to your WorkSpace**

1. From the PCoIP zero client device, choose **Options**, **Configuration**, **Session**, and choose the **OSD: Workspaces Session Settings** connection type\.

1. Enter the registration code from your welcome email\.

1. Enter a name for this registered WorkSpace\.

1. Choose **Connect**\.

## Disconnect from the Zero Client<a name="zero_client_disconnect"></a>

To disconnect the zero client from your WorkSpace, you can press Ctrl\+Alt\+F12\. Alternatively, you can log off of the WorkSpace, which disconnects the client\.