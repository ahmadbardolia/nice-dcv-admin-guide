# Installing an Extended Demo License<a name="setting-up-demo"></a>

When you request an extended demo license from NICE, you receive a `license.lic` file that defines the license\. 

**To install the extended demo license**  
Place the `license.lic` file in the following folder on your server:
+ Windows server

  ```
  C:\Program Files\NICE\DCV\Server\license\license.lic
  ```
+ Linux server

  ```
  /usr/share/dcv/license/license.lic
  ```

Alternatively, to place the `license.lic` in a different folder on the server, you must update the `license-file` configuration parameter so that it specifies the license file's full path\.

**To update the `license-file` configuration parameter on a Windows server**

1. Open the Windows Registry Editor\.

1. Navigate to the **HKEY\_USERS/S\-1\-5\-18/Software/GSettings/com/nicesoftware/dcv/license/** key and select the **license\-file** parameter\.

   If there is no `license-file` parameter in the registry key, create one:

   1. Open the context \(right\-click\) menu for the **license** key in the left\-hand panel and choose **New**, **String Value**\.

   1. For **Name**, type `license-file` and press **Enter**\.

1. Open the **license\-file** parameter\. For **Value data**, type the full path to the `license.lic` file\.

1. Choose **OK** and close the Windows Registry Editor\.

**To update the `license-file` configuration parameter on a Linux server**

1. Navigate to `/etc/dcv/` and open the `dcv.conf` with your preferred text editor\.

1. Locate the `license-file` parameter in the `[license]` section, and replace the existing path with the new full path to the `license.lic` file\.

   If there is no `license-file` parameter in the `[license]` section, add it manually using the following format:

   ```
   license-file = "/custom-path/license.lic"
   ```

1. Save and close the file\.