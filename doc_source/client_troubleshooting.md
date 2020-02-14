# Troubleshooting Amazon WorkSpaces Client Issues<a name="client_troubleshooting"></a>

The following are common issues that you might have with your WorkSpaces client\.

**Topics**
+ [The Amazon WorkSpaces Application Manager client application isn't appearing on my Windows WorkSpace desktop](#no-wam-client)
+ [I don't see any applications listed in the Amazon WorkSpaces Application Manager client application](#no-wam-apps)
+ [After logging in, the Windows client application displays only a white page and I cannot connect to my WorkSpace](#windows_white-page)
+ [My WorkSpaces client gives me a network error, but I am able to use other network\-enabled apps on my device](#net_error)
+ [It sometimes takes several minutes to log in to my Windows WorkSpace](#login_delay)
+ [Sometimes I am logged off of my Windows WorkSpace, even though I closed the session, but did not log off](#logged_out)
+ [I forgot my password and tried to reset it, but I didn’t receive an email with a reset link](#reset_password)
+ [I can't connect to the internet from my WorkSpace](#internet_access)
+ [I installed a third\-party security software package and now I can't connect to my WorkSpace](#security_software)
+ [I am getting a "network connection is slow" warning when connected to my WorkSpace](#latency_warning)
+ [I got an "invalid certificate" error on the client application\. What does that mean?](#client_cert_error)
+ [I'm having trouble when I try to connect to my Windows WorkSpace using Web Access](#webaccess_connection_issues)
+ [I see the following error message: "Device can't connect to the registration service\. Check your network settings\."](#registration_failure)
+ [I am unable to install the Android client application on my Chromebook](#chromebook_android_app)

## The Amazon WorkSpaces Application Manager client application isn't appearing on my Windows WorkSpace desktop<a name="no-wam-client"></a>

The **Amazon WAM** shortcut should be installed on the Windows WorkSpaces client desktop\. If the shortcut isn't on the client desktop, see [Troubleshooting Amazon WAM Issues](https://docs.aws.amazon.com/wam/latest/userguide/troubleshooting.html) in the *Amazon WAM User Guide*\.

## I don't see any applications listed in the Amazon WorkSpaces Application Manager client application<a name="no-wam-apps"></a>

Choose **MY APPS** to see the applications that your admin has specified to install by default on your WorkSpace\. Choose **DISCOVER** to see the applications that your admin has made available for you to install\.

## After logging in, the Windows client application displays only a white page and I cannot connect to my WorkSpace<a name="windows_white-page"></a>

This problem can be caused by expired Verisign/Symantec certificates on your client computer \(not your WorkSpace\)\. Remove the expired certificate and launch the client application again\.

**To find and remove expired Verisign/Symantec certificates**

1. In the Windows **Control Panel** on your client computer \(not your WorkSpace\), choose **Network and Internet**\.

1. Choose **Internet Options**\.

1. In the **Internet Properties** dialog box, choose **Content**, **Certificates**\.

1. In the **Certificates** dialog box, choose the **Intermediate Certificate Authorities** tab\. In the list of certificates, select all certificates that were issued by Verisign or Symantec that are also expired, and choose **Remove**\. Do not remove any certificates that are not expired\.

1. On the **Trusted Root Certificate Authorities** tab, select all certificates that were issued by Verisign or Symantec that are also expired, and choose **Remove**\. Do not remove any certificates that are not expired\.

1. Close the **Certificates** dialog box and the **Internet Properties** dialog box\.

## My WorkSpaces client gives me a network error, but I am able to use other network\-enabled apps on my device<a name="net_error"></a>

The WorkSpaces client applications rely on access to resources in the AWS Cloud, and require a connection that provides at least 1 Mbps download bandwidth\. If your device has an intermittent connection to the network, the WorkSpaces client application might report an issue with the network\.

Amazon WorkSpaces enforces the use of digital certificates issued by Amazon Trust Services, as of May 2018\. Amazon Trust Services is already a trusted Root certificate authority \(CA\) on the operating systems that are supported by Amazon WorkSpaces\. If the Root CA list for your operating system is not up to date, your device cannot connect to WorkSpaces and the client gives a network error\.

**To recognize connection issues due to certificate failures**
+ PCoIP zero clients — The following error message is displayed:

  ```
  Failed to connect. The server provided a certificate that is invalid. See below for details:
  - The supplied certificate is invalid due to timestamp
  - The supplied certificate is not rooted in the devices local certificate store
  ```
+ Other clients — The health checks fail with a red warning triangle for **Internet**\.

**To resolve certificate failures**

Use one of the following solutions for certificate failures\.
+ For the Windows client, download and install the latest Windows client application from [Amazon WorkSpaces Client Downloads](https://clients.amazonworkspaces.com/)\. During installation, the client application ensures that your operating system trusts certificates issued by Amazon Trust Services\. If updating your client does not resolve the issue, contact your Amazon WorkSpaces administrator\.
+ For all other clients, contact your Amazon WorkSpaces administrator\.

## It sometimes takes several minutes to log in to my Windows WorkSpace<a name="login_delay"></a>

Group Policy settings that are set by your system administrator can cause a delay on login after your Windows WorkSpace has been launched or rebooted\. This delay occurs while the Group Policy settings are being applied to the WorkSpace, and is normal\.

## Sometimes I am logged off of my Windows WorkSpace, even though I closed the session, but did not log off<a name="logged_out"></a>

Your system administrator applied a new or updated Group Policy setting to your Windows WorkSpace that requires a logoff of a disconnected session\.

## I forgot my password and tried to reset it, but I didn’t receive an email with a reset link<a name="reset_password"></a>

Contact your Amazon WorkSpaces administrator for assistance\.

## I can't connect to the internet from my WorkSpace<a name="internet_access"></a>

WorkSpaces cannot communicate with the internet by default\. Your Amazon WorkSpaces administrator must explicitly provide internet access\.

## I installed a third\-party security software package and now I can't connect to my WorkSpace<a name="security_software"></a>

You can install any type of security or firewall software on your WorkSpace, but Amazon WorkSpaces requires that certain inbound and outbound ports are open on the WorkSpace\. If the security or firewall software that you install blocks these ports, the WorkSpace might not function correctly or might become unreachable\. For more information, see [Port Requirements for Amazon WorkSpaces](https://docs.aws.amazon.com/workspaces/latest/adminguide/workspaces-port-requirements.html) in the *Amazon WorkSpaces Administration Guide*\.

To restore your WorkSpace, [rebuild your WorkSpace](manage_workspace_client.md#client-rebuild-workspace) if you still have access to it, or ask your Amazon WorkSpaces administrator to rebuild your WorkSpace\. You then have to reinstall the software and properly configure port access for your WorkSpace\.

## I am getting a "network connection is slow" warning when connected to my WorkSpace<a name="latency_warning"></a>

If the round\-trip time from your client to your WorkSpace is longer than 100ms, you can still use your WorkSpace, but this might result in a poor experience\. A slow round\-trip time can be caused by many factors, but the following are the most common causes:
+ You are too far from the AWS Region that your WorkSpace resides in\. For the best WorkSpace experience, you should be within 2,000 miles of the AWS Region that your WorkSpace is in\.
+ Your network connection is inconsistent or slow\. For the best experience, your network connection should provide at least 300 kbps, with capability to provide over 1 Mbps when viewing video or using graphics\-intensive applications on your WorkSpace\.

## I got an "invalid certificate" error on the client application\. What does that mean?<a name="client_cert_error"></a>

The WorkSpaces client application validates the identity of the WorkSpaces service through an SSL/TLS certificate\. If the root certificate authority of the Amazon WorkSpaces service cannot be verified, the client application displays an error and prevents any connection to the service\. The most common cause is a proxy server that is removing the root certificate authority and returning an incomplete certificate to the client application\. Contact your network administrator for assistance\.

## I'm having trouble when I try to connect to my Windows WorkSpace using Web Access<a name="webaccess_connection_issues"></a>

Windows WorkSpaces rely on a specific login screen configuration to enable you to log in from your Web Access client\. Your Amazon WorkSpaces administrator might need to configure Group Policy and Security Policy settings to enable you to log in to your WorkSpace from your Web Access client\. If these settings are not correctly configured, you might experience long login times or black screens when you try to log in to your WorkSpace\. Contact your Amazon WorkSpaces administrator for assistance\.

## I see the following error message: "Device can't connect to the registration service\. Check your network settings\."<a name="registration_failure"></a>

When a registration service failure occurs, you might see the following error message on the **Connection Health Check** page: "Your device is not able to connect to the WorkSpaces Registration service\. You will not be able to register your device with WorkSpaces\. Please check your network settings\."

This error occurs when the WorkSpaces client application can't reach the registration service\. Contact your Amazon WorkSpaces administrator for assistance\.

## I am unable to install the Android client application on my Chromebook<a name="chromebook_android_app"></a>

Version 2\.4\.13 is the final release of the Amazon WorkSpaces Chromebook client application\. For [ Chromebooks that support installing Android applications](https://sites.google.com/a/chromium.org/dev/chromium-os/chrome-os-systems-supporting-android-apps), we recommend using the [Amazon WorkSpaces Android Client Application](amazon-workspaces-android-client.md) instead\.

If you are using a Chromebook launched before 2019, see [ Install Android apps on your Chromebook](https://support.google.com/chromebook/answer/7021273) before attempting to install the Amazon WorkSpaces Android client application\.

In some cases, your WorkSpaces administrator might need to enable your Chromebook to install Android applications\. If you are unable to install the Android client application on your Chromebook, contact your WorkSpaces administrator for assistance\.