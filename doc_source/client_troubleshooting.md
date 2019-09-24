# Troubleshooting Amazon WorkSpaces Client Issues<a name="client_troubleshooting"></a>

The following are common issues that you might have with your WorkSpaces client\.

**Topics**
+ [The Amazon WorkSpaces Application Manager client application isn't appearing on my WorkSpace desktop](#no-wam-client)
+ [I don't see any applications listed in the Amazon WorkSpaces Application Manager client application](#no-wam-apps)
+ [My WorkSpaces client gives me a network error, but I am able to use other network\-enabled apps on my device](#net_error)
+ [It sometimes takes several minutes to log in to my WorkSpace](#login_delay)
+ [Sometimes I am logged off of my WorkSpace, even though I closed the session, but did not log off](#logged_out)
+ [I forgot my password and tried to reset it, but I didn’t receive an email with a reset link](#reset_password)
+ [I can't connect to the internet from my WorkSpace](#internet_access)
+ [I installed a third\-party security software package and now I can't connect to my WorkSpace](#security_software)
+ [I am getting a 'network connection is slow' warning when connected to my WorkSpace](#latency_warning)
+ [I got an invalid certificate error on the client application\. What does that mean?](#client_cert_error)
+ [I'm having trouble when I try to connect to my WorkSpace using Web Access](#webaccess_connection_issues)
+ [I see the following error message: "Your device is not able to connect to the WorkSpaces Registration service\."](#registration_failure)

## The Amazon WorkSpaces Application Manager client application isn't appearing on my WorkSpace desktop<a name="no-wam-client"></a>

The **Amazon WAM** shortcut should be installed on the WorkSpaces client desktop\. If the shortcut isn't on the client desktop, see [Troubleshooting Amazon WAM Issues](https://docs.aws.amazon.com/wam/latest/userguide/troubleshooting.html) in the *Amazon WAM User Guide*\.

## I don't see any applications listed in the Amazon WorkSpaces Application Manager client application<a name="no-wam-apps"></a>

Choose **MY APPS** to see the applications that your admin has specified to install by default on your WorkSpace\. Choose **DISCOVER** to see the applications that your admin has made available for you to install\.

## My WorkSpaces client gives me a network error, but I am able to use other network\-enabled apps on my device<a name="net_error"></a>

The WorkSpaces client applications rely on access to resources in the AWS Cloud, and require a connection that provides at least 1 Mbps download bandwidth\. If your device has an intermittent connection to the network, the WorkSpaces client application might report an issue with the network\.

Amazon WorkSpaces enforces the use of digital certificates issued by Amazon Trust Services, as of May 2018\. Amazon Trust Services is already a trusted Root CA on the operating systems that are supported by Amazon WorkSpaces\. If the Root CA list for your operating system is not up\-to\-date, your device cannot connect to WorkSpaces and the client gives a network error\.

**To recognize connection issues due to certificate failures**
+ PCoIP zero clients — The following error message is displayed:

  ```
  Failed to connect. The server provided a certificate that is invalid. See below for details:
  - The supplied certificate is invalid due to timestamp
  - The supplied certificate is not rooted in the devices local certificate store
  ```
+ Other clients — The health checks fail with a red warning triangle for **Internet**\.

**Topics**
+ [Windows Client Application](#certificate-issues-windows)
+ [PCoIP Zero Clients](#certificate-issues-zero-clients)
+ [Other Client Applications](#certificate-issues-other)

### Windows Client Application<a name="certificate-issues-windows"></a>

Use one of the following solutions for certificate failures\.

**Solution 1: Update the client application**  
Download and install the latest Windows client application from [Amazon WorkSpaces Client Downloads](http://clients.amazonworkspaces.com/)\. During installation, the client application ensures that your operating system trusts certificates issued by Amazon Trust Services\.

**Solution 2: Add Amazon Trust Services to the local Root CA list**

1. Open [https://www\.amazontrust\.com/repository/](https://www.amazontrust.com/repository/)\.

1. Download the Starfield certificate in DER format \(2b071c59a0a0ae76b0eadb2bad23bad4580b69c3601b630c2eaf0613afa83f92\)\.

1. Open the Microsoft Management Console\. \(From a Command Prompt window, run mmc\.\)

1. Choose **File**, **Add/Remove Snap\-in**, **Certificates**, **Add**\.

1. On the **Certificates snap\-in** page, select **Computer account** and choose **Next**\. Keep the default, **Local computer**\. Choose **Finish**\. Choose **OK**\.

1. Expand **Certificates \(Local Computer\)** and select **Trusted Root Certification Authorities**\. Choose **Action**, **All Tasks**, **Import**\.

1. Follow the wizard to import the certificate that you downloaded\.

1. Exit and restart the WorkSpaces client application\.

**Solution 3: Deploy Amazon Trust Services as a trusted CA using Group Policy**  
Add the Starfield certificate to the trusted Root CAs for the domain using Group Policy\. For more information, see [Use Policy to Distribute Certificates](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772491(v=ws.11))\.

### PCoIP Zero Clients<a name="certificate-issues-zero-clients"></a>

To connect directly to a WorkSpace using firmware version 6\.0 or later, download and install the certificate issued by Amazon Trust Services\.

**To add Amazon Trust Services as a trusted Root CA**

1. Open [https://certs\.secureserver\.net/repository/](https://certs.secureserver.net/repository/)\.

1. Download the certificate under **Starfield Certificate Chain** with the thumbprint 14 65 FA 20 53 97 B8 76 FA A6 F0 A9 95 8E 55 90 E4 0F CC 7F AA 4F B7 C2 C8 67 75 21 FB 5F B6 58\.

1. Upload the certificate to the zero client\. For more information, see [Uploading Certificates](http://www.teradici.com/web-help/TER1504003/6.0/default.htm#05_Managing/04_UploadCertificate.htm) in the Teradici documentation\.

### Other Client Applications<a name="certificate-issues-other"></a>

Add the Starfield certificate \(2b071c59a0a0ae76b0eadb2bad23bad4580b69c3601b630c2eaf0613afa83f92\) from [Amazon Trust Services](https://www.amazontrust.com/repository/)\. For more information about how to add a Root CA, see the following documentation:
+ Android: [Add & remove certificates](https://support.google.com/nexus/answer/2844832)
+ Chrome OS: [Manage client certificates on Chrome devices](https://support.google.com/chrome/a/answer/6080885)
+ macOS and iOS: [Installing a CA's Root Certificate on Your Test Device](https://developer.apple.com/library/content/qa/qa1948/_index.html#//apple_ref/doc/uid/DTS40017603-CH1-SECINSTALLING)

## It sometimes takes several minutes to log in to my WorkSpace<a name="login_delay"></a>

Group Policy settings set by your system administrator can cause a delay on login after your WorkSpace has been launched or rebooted\. This delay occurs while the Group Policy settings are being applied to the WorkSpace, and is normal\.

## Sometimes I am logged off of my WorkSpace, even though I closed the session, but did not log off<a name="logged_out"></a>

Your system administrator applied a new or updated Group Policy setting to your WorkSpace that requires a logoff of a disconnected session\.

## I forgot my password and tried to reset it, but I didn’t receive an email with a reset link<a name="reset_password"></a>

Contact your Amazon WorkSpaces administrator for assistance\.

## I can't connect to the internet from my WorkSpace<a name="internet_access"></a>

WorkSpaces cannot communicate with the internet by default\. Your administrator must explicitly provide internet access\.

## I installed a third\-party security software package and now I can't connect to my WorkSpace<a name="security_software"></a>

You can install any type of security or firewall software on your WorkSpace, but Amazon WorkSpaces requires that certain inbound and outbound ports are open on the WorkSpace\. If the security or firewall software that you install blocks these ports, the WorkSpace might not function correctly or might become unreachable\. For more information, see [Port Requirements for Amazon WorkSpaces](https://docs.aws.amazon.com/workspaces/latest/adminguide/workspaces-port-requirements.html) in the *Amazon WorkSpaces Administration Guide*\.

To restore your WorkSpace, ask your administrator to rebuild your WorkSpace\. You then have to re\-install the software and properly configure port access for your WorkSpace\.

## I am getting a 'network connection is slow' warning when connected to my WorkSpace<a name="latency_warning"></a>

If the round\-trip time from your client to your WorkSpace is longer than 100ms, you can still use your WorkSpace, but this might result in a poor experience\. A slow round\-trip time can be caused by many factors, but the following are the most common:
+ You are too far from the AWS Region that your WorkSpace resides in\. For the best WorkSpace experience, you should be within 2000 miles of the AWS Region that your WorkSpace is in\.
+ Your network connection is inconsistent or slow\. For the best experience, your network connection should provide at least 300 kbps, with capability to provide over 1 Mbps when viewing video or using graphics intensive applications on your WorkSpace\.

## I got an invalid certificate error on the client application\. What does that mean?<a name="client_cert_error"></a>

The WorkSpaces client application validates the identity of the WorkSpaces service through an SSL certificate\. If the root certificate authority of the Amazon WorkSpaces service cannot be verified, the client application displays an error and prevents any connection to the service\. The most common cause is a proxy server that is removing the root certificate authority and returning an incomplete certificate to the client application\. Contact your network administrator for additional help\.

## I'm having trouble when I try to connect to my WorkSpace using Web Access<a name="webaccess_connection_issues"></a>

Some WorkSpaces rely on a specific login screen configuration to enable you to log in from your Web Access client\. For example, depending on the type of WorkSpace, your network administrator might need to configure a Group Policy setting and a Local Security Policy setting to enable you to log in to your WorkSpace from your Web Access client\. If these two settings are not correctly configured, you might experience long login times or black screens when you try to log in to your WorkSpace\. Contact your network administrator for additional help\. 

## I see the following error message: "Your device is not able to connect to the WorkSpaces Registration service\."<a name="registration_failure"></a>

When registration service failure occurs, you might see the following error message on the **Connection Health Check** page: "Your device is not able to connect to the WorkSpaces Registration service\. You will not be able to register your device with WorkSpaces\. Please check your network settings\."

This error occurs when the WorkSpaces client application can't reach the registration service\. Typically, this happens when the WorkSpaces directory has been deleted\. To resolve this error, make sure that the registration code is valid and corresponds to a running directory in the AWS Cloud\.