# Troubleshooting Amazon WorkSpaces Client Issues<a name="client_troubleshooting"></a>

The following are common issues that you might have with your WorkSpaces client\.


+ [My WorkSpaces client gives me a network error, but I am able to use other network enabled apps on my device](#net_error)
+ [It sometimes takes several minutes to log in to my WorkSpace](#login_delay)
+ [Sometimes I am logged off of my WorkSpace, even though I closed the session, but did not log off](#logged_out)
+ [I can't connect to the Internet from my WorkSpace](#internet_access)
+ [I installed a third\-party security software package and now I can't connect to my WorkSpace](#security_software)
+ [I am getting a 'network connection is slow' warning when connected to my WorkSpace](#latency_warning)
+ [I got an invalid certificate error on the client application\. What does that mean?](#client_cert_error)
+ [I see the following error message: "Your device is not able to connect to the WorkSpaces Registration service\."](#registration_failure)

## My WorkSpaces client gives me a network error, but I am able to use other network enabled apps on my device<a name="net_error"></a>

The WorkSpaces client applications rely on access to resources in the AWS cloud and require a connection that provides at least 1 Mbps download bandwidth\. If your device has an intermittent connection to the network, the WorkSpaces client application may report an issue with the network\.

If you have a stable internet connection but your client reports an issue with your internet connection, verify that the root certificates for your operating system are up\-to\-date or contact your system administrator for assistance\. Any operating system released or updated after 2007 trusts the certificates used by Amazon WorkSpaces\. If you choose to manually add the required root certificates, use the following instructions\.

WorkSpaces use ATS certificates issued by CAs that chain from one of the following root CAs:

+ Amazon Root CA 1

+ Amazon Root CA 2

+ Amazon Root CA 3

+ Amazon Root CA 4

These root certificates are cross\-signed by the following root CAs:

+ Starfield Services Root Certificate Authority \- G2

+ Starfield Class 2 Certificate Authority

If your trust store contains either the Amazon or Starfield root certificates, WorkSpaces work with your system\. Otherwise, you must add them from [Amazon Trust Services](https://www.amazontrust.com/repository/)\.

To add certificates to your local operating system, see the following documentation:

+ Android: [Add & remove certificates](https://support.google.com/nexus/answer/2844832)

+ Chrome OS: [Manage client certificates on Chrome devices](https://support.google.com/chrome/a/answer/6080885)

+ Mac OS/iOS: [Installing a CA's Root Certificate on Your Test Device](https://developer.apple.com/library/content/qa/qa1948/_index.html#//apple_ref/doc/uid/DTS40017603-CH1-SECINSTALLING)

+ Windows: [Manage Trusted Root Certificates](https://technet.microsoft.com/en-us/library/cc754841.aspx)

## It sometimes takes several minutes to log in to my WorkSpace<a name="login_delay"></a>

Group Policy settings set by your system administrator can cause a delay on login after your WorkSpace has been launched or rebooted\. This delay occurs while the Group Policy settings are being applied to the WorkSpace and is normal\.

## Sometimes I am logged off of my WorkSpace, even though I closed the session, but did not log off<a name="logged_out"></a>

Your system administrator applied a new or updated Group Policy setting to your WorkSpace that requires a logoff of a disconnected session\.

## I can't connect to the Internet from my WorkSpace<a name="internet_access"></a>

WorkSpaces cannot communicate with the Internet by default\. Your administrator must explicitly provide Internet access\.

## I installed a third\-party security software package and now I can't connect to my WorkSpace<a name="security_software"></a>

You can install any type of security or firewall software on your WorkSpace, but Amazon WorkSpaces requires that certain inbound and outbound ports are open on the WorkSpace\. If the security or firewall software that you install blocks these ports, the WorkSpace might not function correctly or might become unreachable\. For more information, see [Port Requirements for Amazon WorkSpaces](http://docs.aws.amazon.com/workspaces/latest/adminguide/workspaces-port-requirements.html) in the *Amazon WorkSpaces Administration Guide*\.

To restore your WorkSpace, ask your administrator to rebuild your WorkSpace\. You will have to re\-install the software and properly configure port access for your WorkSpace\.

## I am getting a 'network connection is slow' warning when connected to my WorkSpace<a name="latency_warning"></a>

If the roundtrip time from your client to your WorkSpace is longer than 100ms, you can still use your WorkSpace, but this may result in a poor experience\. A slow roundtrip time can be caused by many factors, but the following are the most common:

+ You are too far from the AWS region that your WorkSpace resides in\. For the best WorkSpace experience, you should be within 2000 miles of the AWS region that your WorkSpace is in\.

+ Your network connection is inconsistent or slow\. For the best experience, your network connection should provide at least 300 kbps, with capability to provide over 1 Mbps when viewing video or using graphics intensive applications on your WorkSpace\.

## I got an invalid certificate error on the client application\. What does that mean?<a name="client_cert_error"></a>

The WorkSpaces client application validates the identity of the WorkSpaces service through an SSL certificate\. If the root certificate authority of the Amazon WorkSpaces service cannot be verified, the client application displays an error and prevents any connection to the service\. The most common cause is a proxy server that is removing the root certificate authority and returning an incomplete certificate to the client application\. Contact your network administrator for additional help\.

## I see the following error message: "Your device is not able to connect to the WorkSpaces Registration service\."<a name="registration_failure"></a>

When registration service failure occurs, you might see the following error message on the **Connection Health Check** page: "Your device is not able to connect to the WorkSpaces Registration service\. You will not be able to register your device with WorkSpaces\. Please check your network settings\."

This error occurs when the WorkSpaces client application can't reach the registration service\. Typically, this happens when the WorkSpaces directory has been deleted\. To resolve this error, make sure that the registration code is valid and corresponds to a running directory in the AWS cloud\.