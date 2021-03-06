# Managing NICE DCV Sessions<a name="managing-sessions"></a>

You must create a NICE DCV session on your NICE DCV server that your clients can connect to\. Clients can only connect to a NICE DCV server if there is an active session\.

**Topics**
+ [Introduction to NICE DCV sessions](#managing-sessions-intro)
+ [Using the Command Line Tool to Manage NICE DCV sessions](#managing-sessions-cli)
+ [Starting NICE DCV Sessions](managing-sessions-start.md)
+ [Stopping NICE DCV Sessions](managing-sessions-lifecycle-stop.md)
+ [Viewing NICE DCV Sessions](managing-sessions-lifecycle-view.md)

## Introduction to NICE DCV sessions<a name="managing-sessions-intro"></a>

Every NICE DCV session has the following attributes:
+ **ID** — Used to uniquely identify the session on the NICE DCV server\.
+ **Owner** — The NICE DCV user who created the session\. By default, only the owner can connect to the session\.

NICE DCV clients need this information to connect to the session\.

NICE DCV offers two types of sessions:

### Console Sessions<a name="managing-sessions-intro-console"></a>

Console sessions are supported on Windows and Linux NICE DCV servers\.

Only one console session can be hosted on the NICE DCV server at a time\. Console sessions are created and managed by the Administrator on Windows NICE DCV servers, and the root user on Linux NICE DCV servers\. 

**Note**  
You can't run console and virtual sessions on the same NICE DCV server at the same time\.

### Virtual Sessions<a name="managing-sessions-intro-virtual"></a>

Virtual sessions are supported on Linux NICE DCV servers only\.

A NICE DCV server can host multiple virtual sessions simultaneously\. Virtual sessions are created and managed by NICE DCV users\. NICE DCV users can only manage sessions that they have created\. The root user can manage all virtual sessions that are currently running on the NICE DCV server\.

To use virtual sessions, ensure that you have properly installed and configured an X server\. A new virtual X server instance is created for each session\. Each session uses the display provided by its virtual server\. This enables you to host multiple virtual sessions on a single NICE DCV server\. To share hardware\-based OpenGL across multiple virtual sessions, you must connect the virtual X server instance to the GPU by configuring the `dcv-gl.conf` file\.

**Note**  
You can't run console and virtual sessions on the same NICE DCV server at the same time\.

## Using the Command Line Tool to Manage NICE DCV sessions<a name="managing-sessions-cli"></a>

The NICE DCV server ships with a command line tool that can be used to start, stop, and view NICE DCV sessions\.

To use the command line tool on a Windows NICE DCV server, navigate to the folder in which the `dcv.exe` file is located, `C:\Program Files\NICE\DCV\Server\bin\` by default, and open a command prompt window\.

On Linux NICE DCV servers, the command line tool is automatically configured in the `$PATH` environment variable\. This enables you to use the command line tool from any folder\. Open a terminal window and type the command to execute\.