# Manage Your WorkSpace from Your Client<a name="manage_workspace_client"></a>

If you use the [Windows client ](amazon-workspaces-windows-client.md) or the [OS X client ](amazon-workspaces-osx-client.md) for Amazon WorkSpaces, you can perform the following management tasks directly from your client\. 

**Note**  
You can perform these tasks only if they are enabled by your Amazon WorkSpaces administrator\.

**Topics**
+ [Use **Remember Me** to Save Your Credentials](#client-save-credentials)
+ [Restart Your WorkSpace](#client-restart-workspace)
+ [Increase Your WorkSpace Disk Size](#client-increase-disk-workspace)
+ [Change Your WorkSpace Compute Type](#client-change-compute-type)
+ [Switch Your WorkSpace Running Mode](#client-switch-running-mode)
+ [Rebuild Your WorkSpace](#client-switch-running-mode)

## Use **Remember Me** to Save Your Credentials<a name="client-save-credentials"></a>

You can choose whether to save your credentials securely so that you can reconnect to your WorkSpace without re\-entering your credentials while the client application remains running\. Your credentials are securely cached in RAM only\. You can disable **Remember Me** and enable it again at any time\.

**To use Remember Me to save your credentials**

1. Open your Amazon WorkSpaces client\.

1. On the client login screen, choose the gear icon \(Windows\) or the **Option** menu \(Mac\), and choose **Advanced Settings**\.

1. Select or clear the **Remember Me** check box to enable or disable this option as required\.

## Restart Your WorkSpace<a name="client-restart-workspace"></a>

If you are experiencing issues with your WorkSpace, you can restart it\. Restarting a WorkSpace disconnects you from your WorkSpace, so that it can be shut down and restarted\. To avoid losing changes, save any open documents and other application files before you restart your WorkSpace\. Your user data, operating system, and system settings are not affected\.

**To restart your WorkSpace**

1. Open your Amazon WorkSpaces client and connect to your WorkSpace\.

1. Choose **Amazon WorkSpaces**, **Restart WorkSpace**\. 

1. When prompted to restart your WorkSpace, choose **Restart**\.

1. After you are disconnected from your WorkSpace, the client application login screen remains open\. You can log back into your WorkSpace, or close the screen\.

## Increase Your WorkSpace Disk Size<a name="client-increase-disk-workspace"></a>

You can increase your WorkSpace disk size to add more storage capacity\. You can increase the size of your C: drive up to 175 GB, and the size of your D: drive up to 100 GB without contacting your administrator\. If your administrator recently created your WorkSpace, you must wait 6 hours before you can increase your WorkSpace disk size\. After that, you can do so once in a 6\-hour period\. 

When your WorkSpace disk size increase is in progress, you can perform most tasks on your WorkSpace\. However, you can't change your WorkSpace compute type, switch the WorkSpace running mode, rebuild your WorkSpace, and restart your WorkSpace\. This process may take up to an hour\.

**Note**  
 You can only resize SSD volumes\. Also, increasing your WorkSpace disk size will increase the amount that your organization pays for your WorkSpace\. 

**To increase your WorkSpace disk size**

1. Open your Amazon WorkSpaces client and connect to your WorkSpace\.

1. Choose **My WorkSpace**, **Increase disk size**\. 

1. In the **Increase disk size** dialog box, the current disk size of your C: drive and D: drive displays\. It also displays the amount by which your storage increases, if you proceed with the disk size increase\. 

1. To proceed with the disk size increase, choose **Increase**\. 

1. A message displays information about the disk size increase process\. Review the information, and choose **Close**\.

## Change Your WorkSpace Compute Type<a name="client-change-compute-type"></a>

You can change your WorkSpace compute type to choose a different bundle for your WorkSpace\. If your administrator recently created your WorkSpace, you must wait 6 hours before you can change your WorkSpace compute type\. After that, you can switch to a larger compute type once in a 6\-hour period, or to a smaller compute type once in a 30\-day period\.

When your WorkSpace compute type change is in progress, you are disconnected from the WorkSpace\. During this time, you can't use or make changes to the WorkSpace\. To avoid losing changes, save any open documents and other application files before you change your WorkSpace compute type\. This process may take up to an hour\.

**Note**  
Changing your WorkSpace compute type will change the amount that your organization pays for your WorkSpace\. 

**To change your WorkSpace compute type**

1. Open your Amazon WorkSpaces client and connect to your WorkSpace\.

1. Choose **My WorkSpace**, **Change compute type**\. 

1. In the **Change compute type** dialog box, the current compute type for your WorkSpace displays\. Choose a different compute type from the list, and then choose **Update**\.

1. A message displays information about the compute type change process\. Review the information, and choose **Update**\.

## Switch Your WorkSpace Running Mode<a name="client-switch-running-mode"></a>

You can change your WorkSpace running mode to determine if your WorkSpace is always running or stops after a specified period of inactivity\. Amazon WorkSpaces provides the following two running modes that you can choose from:
+ **Always On** — Keeps your WorkSpace always running\. 
+ **AutoStop** — Your WorkSpace starts when you sign in and stops after a specified period of inactivity\. After your WorkSpace stops, the state of your apps and data is saved\. 

**Note**  
Switching your WorkSpace running mode will change the amount that your organization pays for your WorkSpace\. 

**To switch your WorkSpace running mode**

1. Open your Amazon WorkSpaces client and connect to your WorkSpace\.

1. Choose **My WorkSpace**, **Switch running mode**\. 

1. In the **Switch running mode** dialog box, choose a different running mode, and then choose **Switch**\.

1. A message confirms your choice\. Choose **Close**\.

## Rebuild Your WorkSpace<a name="client-switch-running-mode"></a>

You can rebuild your WorkSpace to restore the operating system running on the WorkSpace to its original state\.

If you want to rebuild your WorkSpace to resolve an issue that you are experiencing with the WorkSpace, try restarting it first\. If you rebuild your WorkSpace, any applications that you installed and system settings that you configured after the WorkSpace was created are lost\. When a WorkSpace is rebuilt, the D: drive is recreated from the latest backup\. Because backups are completed every 12 hours, your data may be up to 12 hours old\. If your administrator recently created your WorkSpace, you must wait 12 hours before you can rebuild your WorkSpace\. 

While your WorkSpace rebuild is in progress, you are disconnected from the WorkSpace\. During this time, you can't use or make changes to the WorkSpace\. To avoid losing changes, save any open documents and other application files before you rebuild your WorkSpace\. This process may take up to an hour\.

**To rebuild your WorkSpace**

1. Open your Amazon WorkSpaces client and connect to your WorkSpace\.

1. Choose **My WorkSpace**, **Rebuild WorkSpace**\. 

1. In the **Rebuild WorkSpace** dialog box, review the information\. If you choose to proceed with the rebuild, choose **Rebuild**\.