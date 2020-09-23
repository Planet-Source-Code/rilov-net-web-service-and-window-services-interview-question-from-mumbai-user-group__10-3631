<div align="center">

## Net Web Service and Window Services Interview Question From Mumbai User Group


</div>

### Description

Net Web Service and Window Services Interview Question From Mumbai User Group
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Rilov](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/rilov.md)
**Level**          |Advanced
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |C\#, VB\.NET, ASP\.NET
**Category**       |[Server Side](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/server-side__10-31.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/rilov-net-web-service-and-window-services-interview-question-from-mumbai-user-group__10-3631/archive/master.zip)





### Source Code

```

<table border="1" width="100%" bgcolor="#C0C0C0" bordercolor="#000080" height="4991">
 <tr>
 <td width="100%" bgcolor="#FF9933" height="1"><font face="Verdana" size="2" color="#000080"><b>What is
  WSDL</b><br>
  WSDL is the Web Service Description Language, and it is implemented as a
  specific XML vocabulary. While it's very much more complex than what can
  be described here, there are two important aspects to WSDL with which you
  should be aware. First, WSDL provides instructions to consumers of Web
  Services to describe the layout and contents of the SOAP packets the Web
  Service intends to issue. It's an interface description document, of
  sorts. And second, it isn't intended that you read and interpret the WSDL.
  Rather, WSDL should be processed by machine, typically to generate proxy
  source code (.NET) or create dynamic proxies on the fly (the SOAP Toolkit
  or Web Service Behavior). <br>
  <br>
  <br>
  <b>2.What is a Windows Service and how does its lifecycle differ from a
  "standard" EXE?</b><br>
  <br>
  Windows service is a application that runs in the background. It is
  equivalent to a NT service. The executable created is not a Windows
  application, and hence you can't just click and run it . it needs to be
  installed as a service, VB.Net has a facility where we can add an
  installer to our program and then use a utility to install the service.
  Where as this is not the case with standard exe<br>
  <br>
  How can a win service developed in .NET be installed or used in Win98?<br>
  Windows service cannot be installed on Win9x machines even though the .NET
  framework runs on machine.</font>
  <blockquote>
  <p><font face="Verdana" size="2" color="#000080"><b>Can you debug a
  Windows Service? How ? <br>
  </b>Yes we can debug a Windows Service.<br>
  Attach the WinDbg debugger to a service after the service starts <br>
  This method is similar to the method that you can use to attach a
  debugger to a process and then debug a process. <br>
  Use the process ID of the process that hosts the service that you want
  to debug <br>
  1 To determine the process ID (PID) of the process that hosts the
  service that you want to debug, use one of the following methods. <br>
  <b>• Method 1: Use the Task Manager <br>
  </b>a. Right-click the taskbar, and then click Task Manager. The Windows
  Task Manager dialog box appears.<br>
  b. Click the Processes tab of the Windows Task Manager dialog box.<br>
  c. Under Image Name, click the image name of the process that hosts the
  service that you want to debug. Note the process ID of this process as
  specified by the value of the corresponding PID field.<br>
  • Method 2: Use the Task List Utility (tlist.exe) <br>
  a. Click Start, and then click Run. The Run dialog box appears.<br>
  b. In the Open box, type cmd, and then click OK.<br>
  c. At the command prompt, change the directory path to reflect the
  location of the tlist.exe file on your computer.<br>
  <br>
  Note The tlist.exe file is typically located in the following directory:
  C:\Program Files\Debugging Tools for Windows<br>
  d. At the command prompt, type tlist to list the image names and the
  process IDs of all processes that are currently running on your
  computer.<br>
  <br>
  Note Make a note of the process ID of the process that hosts the service
  that you want to debug.<br>
  2 At a command prompt, change the directory path to reflect the location
  of the windbg.exe file on your computer. <br>
  <br>
  Note If a command prompt is not open, follow steps a and b of Method 1.
  The windbg.exe file is typically located in the following directory:
  C:\Program Files\Debugging Tools for Windows. <br>
  3 At the command prompt, type windbg –p ProcessID to attach the WinDbg
  debugger to the process that hosts the service that you want to debug. <br>
  <br>
  Note ProcessID is a placeholder for the process ID of the process that
  hosts the service that you want to debug. <br>
  <br>
  Use the image name of the process that hosts the service that you want
  to debug<br>
  <br>
  You can use this method only if there is exactly one running instance of
  the process that hosts the service that you want to run. To do this,
  follow these steps: <br>
  1 Click Start, and then click Run. The Run dialog box appears. <br>
  2 In the Open box, type cmd, and then click OK to open a command prompt.
  <br>
  3 At the command prompt, change the directory path to reflect the
  location of the windbg.exe file on your computer. <br>
  <br>
  Note The windbg.exe file is typically located in the following
  directory: C:\Program Files\Debugging Tools for Windows. <br>
  4 At the command prompt, type windbg –pn ImageName to attach the
  WinDbg debugger to the process that hosts the service that you want to
  debug. <br>
  <br>
  NoteImageName is a placeholder for the image name of the process that
  hosts the service that you want to debug. The &quot;-pn&quot;
  command-line option specifies that the ImageName command-line argument
  is the image name of a process. <br>
  back to the top <br>
  Start the WinDbg debugger and attach to the process that hosts the
  service that you want to debug<br>
  <br>
  1 Start Windows Explorer. <br>
  2 Locate the windbg.exe file on your computer. <br>
  <br>
  Note The windbg.exe file is typically located in the following
  directory: C:\Program Files\Debugging Tools for Windows <br>
  3 Run the windbg.exe file to start the WinDbg debugger. <br>
  4 On the File menu, click Attach to a Process to display the Attach to
  Process dialog box. <br>
  5 Click to select the node that corresponds to the process that hosts
  the service that you want to debug, and then click OK. <br>
  6 In the dialog box that appears, click Yes to save base workspace
  information. Notice that you can now debug the disassembled code of your
  service. <br>
  Configure a service to start with the WinDbg debugger attached <br>
  You can use this method to debug services if you want to troubleshoot
  service-startup-related problems. <br>
  1 Configure the "Image File Execution" options. To do this,
  use one of the following methods: </font></p>
  <p><font face="Verdana" size="2" color="#000080">• Method 1: Use the
  Global Flags Editor (gflags.exe) <br>
  a. Start Windows Explorer.<br>
  b. Locate the gflags.exe file on your computer.<br>
  <br>
  Note The gflags.exe file is typically located in the following
  directory: C:\Program Files\Debugging Tools for Windows.<br>
  c. Run the gflags.exe file to start the Global Flags Editor.<br>
  d. In the Image File Name text box, type the image name of the process
  that hosts the service that you want to debug. For example, if you want
  to debug a service that is hosted by a process that has MyService.exe as
  the image name, type MyService.exe.<br>
  e. Under Destination, click to select the Image File Options option.<br>
  f. Under Image Debugger Options, click to select the Debugger check box.<br>
  g. In the Debugger text box, type the full path of the debugger that you
  want to use. For example, if you want to use the WinDbg debugger to
  debug a service, you can type a full path that is similar to the
  following: C:\Program Files\Debugging Tools for Windows\windbg.exe<br>
  h. Click Apply, and then click OK to quit the Global Flags Editor.<br>
  • Method 2: Use Registry Editor <br>
  a. Click Start, and then click Run. The Run dialog box appears.<br>
  b. In the Open box, type regedit, and then click OK to start Registry
  Editor.<br>
  c. Warning If you use Registry Editor incorrectly, you may cause serious
  problems that may require you to reinstall your operating system.
  Microsoft cannot guarantee that you can solve problems that result from
  using Registry Editor incorrectly. Use Registry Editor at your own risk.</font></p>
  </blockquote>
  <p><font face="Verdana" size="2" color="#000080"><br>
  In Registry Editor, locate, and then right-click the following registry
  subkey:<br>
  HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File
  Execution Options<br>
  d. Point to New, and then click Key. In the left pane of Registry Editor,
  notice that New Key #1 (the name of a new registry subkey) is selected for
  editing.<br>
  e. Type ImageName to replace New Key #1, and then press ENTER.<br>
  <br>
  Note ImageName is a placeholder for the image name of the process that
  hosts the service that you want to debug. For example, if you want to
  debug a service that is hosted by a process that has MyService.exe as the
  image name, type MyService.exe.<br>
  f. Right-click the registry subkey that you created in step e.<br>
  g. Point to New, and then click String Value. In the right pane of
  Registry Editor, notice that New Value #1, the name of a new registry
  entry, is selected for editing.<br>
  h. Replace New Value #1 with Debugger, and then press ENTER.<br>
  i. Right-click the Debugger registry entry that you created in step h, and
  then click Modify. The Edit String dialog box appears.<br>
  j. In the Value data text box, type DebuggerPath, and then click OK.<br>
  <br>
  Note DebuggerPath is a placeholder for the full path of the debugger that
  you want to use. For example, if you want to use the WinDbg debugger to
  debug a service, you can type a full path that is similar to the
  following: C:\Program Files\Debugging Tools for Windows\windbg.exe<br>
  2 For the debugger window to appear on your desktop, and to interact with
  the debugger, make your service interactive. If you do not make your
  service interactive, the debugger will start but you cannot see it and you
  cannot issue commands. To make your service interactive, use one of the
  following methods: <br>
  • Method 1: Use the Services console <br>
  a. Click Start, and then point to Programs.<br>
  b. On the Programs menu, point to Administrative Tools, and then click
  Services. The Services console appears.<br>
  c. In the right pane of the Services console, right-click ServiceName, and
  then click Properties.<br>
  <br>
  Note ServiceName is a placeholder for the name of the service that you
  want to debug.<br>
  d. On the Log On tab, click to select the Allow service to interact with
  desktop check box under Local System account, and then click OK.<br>
  • Method 2: Use Registry Editor <br>
  a. In Registry Editor, locate, and then click the following registry subkey:<br>
  HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\ServiceName<br>
  Note Replace ServiceName with the name of the service that you want to
  debug. For example, if you want to debug a service named MyService, locate
  and then click the following registry key:<br>
  HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\MyService<br>
  b. Under the Name field in the right pane of Registry Editor, right-click
  Type, and then click Modify. The Edit DWORD Value dialog box appears.<br>
  c. Change the text in the Value data text box to the result of the binary
  OR operation with the binary value of the current text and the binary
  value, 0x00000100, as the two operands. The binary value, 0x00000100,
  corresponds to the SERVICE_INTERACTIVE_PROCESS constant that is defined in
  the WinNT.h header file on your computer. This constant specifies that a
  service is interactive in nature.<br>
  3 When a service starts, the service communicates to the Service Control
  Manager how long the service must have to start (the time-out period for
  the service). If the Service Control Manager does not receive a
  "service started" notice from the service within this time-out
  period, the Service Control Manager terminates the process that hosts the
  service. This time-out period is typically less than 30 seconds. If you do
  not adjust this time-out period, the Service Control Manager ends the
  process and the attached debugger while you are trying to debug. To adjust
  this time-out period, follow these steps: <br>
  a. In Registry Editor, locate, and then right-click the following registry
  subkey: <br>
  HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control <br>
  b. Point to New, and then click DWORD Value. In the right pane of Registry
  Editor, notice that New Value #1 (the name of a new registry entry) is
  selected for editing. <br>
  c. Type ServicesPipeTimeout to replace New Value #1, and then press ENTER.
  <br>
  d. Right-click the ServicesPipeTimeout registry entry that you created in
  step c, and then click Modify. The Edit DWORD Value dialog box appears. <br>
  e. In the Value data text box, type TimeoutPeriod, and then click OK <br>
  <br>
  Note TimeoutPeriod is a placeholder for the value of the time-out period
  (in milliseconds) that you want to set for the service. For example, if
  you want to set the time-out period to 24 hours (86400000 milliseconds),
  type 86400000. <br>
  f. Restart the computer. You must restart the computer for Service Control
  Manager to apply this change. <br>
  4 Start your Windows service. To do this, follow these steps: <br>
  a. Click Start, and then point to Programs. <br>
  b. On the Programs menu, point to Administrative Tools, and then click
  Services. The Services console appears. <br>
  c. In the right pane of the Services console, right-click ServiceName, and
  then click Start. <br>
  <br>
  Note ServiceName is a placeholder for the name of the service that you
  want to debug. <br>
  </font></td>
 </tr>
 <tr>
 <td width="100%" bgcolor="#FFFFFF" height="68"><font face="Verdana" size="2" color="#000080"><b>Can you give an example of when it would be appropriate to use a web
  service as opposed to non-serviced</b> <b>.NET component</b><br>
  Web service is one of main component in Service Oriented Architecture. You
  could use web services when your clients and servers are running on
  different networks and also different platforms. This provides a loosely
  coupled system. And also if the client is behind the firewall it would be
  easy to use web service since it runs on port 80 (by default) instead of
  having some thing else in Service Oriented Architecture applications.<br>
  <b>What is the standard you use to wrap up a call to a Web service<br>
  </b>"SOAP.<br>
  "<br>
  <b>What is the transport protocol you use to call a Web service SOAP<br>
  </b>HTTP with SOAP<br>
  <br>
  <b>What does WSDL stand for? <br>
  </b>&quot;WSDL stands for Web Services Dsescription Langauge. There is
  WSDL.exe that creates a .wsdl Files which defines how an XML Web service
  behaves and instructs clients as to how to interact with the service.<br>
  eg: wsdl http://LocalHost/WebServiceName.asmx&quot;<br>
  <br>
  <b>Where on the Internet would you look for Web Services?</b><br>
  www.uddi.org
  </font>
  <p><font face="Verdana" size="2" color="#000080">
  <b>What does WSDL stand for? </b><br>
  Web Services Description Language<br>
  <br>
  <b>True or False: To test a Web service you must create a windows
  application or Web application to consume this service? </b><br>
  False.<br>
  <br>
  <b>What are the various ways of accessing a web service ?</b><br>
  1.Asynchronous Call<br>
  Application can make a call to the Webservice and then continue todo
  watever oit wants to do.When the service is ready it will notify the
  application.Application can use BEGIN and END method to make asynchronous
  call to the webmethod.We can use either a WaitHandle or a Delegate object
  when making asynchronous call.<br>
  The WaitHandle class share resources between several objects. It provides
  several methods which will wait for the resources to become available<br>
  The easiest and most powerful way to to implement an asynchronous call is
  using a delegate object. A delegate object wraps up a callback function.
  The idea is to pass a method in the invocation of the web method. When the
  webmethod has finished it will call this callback function to process the
  result<br>
  <br>
  2.Synchronous Call<br>
  Application has to wait until execution has completed.<br>
  <br>
  <br>
  <br>
  <b>What are VSDISCO files?</b><br>
  VSDISCO files are DISCO files that support dynamic discovery of Web
  services. If you place the following VSDISCO file in a directory on your
  Web server, for example, it returns references to all ASMX and DISCO files
  in the host directory and any subdirectories not noted in
  <EXCLUDE>elements:<br>
  <br>
  <DYNAMICDISCOVERY<br>
  xmlns=&quot;urn:schemas-dynamicdiscovery:disco.2000-03-17&quot;&gt;<br>
  <EXCLUDE path="_vti_script" />
  <br>
  <b>How does dynamic discovery work?</b><br>
  ASP.NET maps the file name extension VSDISCO to an HTTP handler that scans
  the host directory and subdirectories for ASMX and DISCO files and returns
  a dynamically generated DISCO document. A client who requests a VSDISCO
  file gets back what appears to be a static DISCO document.<br>
  <br>
  Note that VSDISCO files are disabled in the release version of ASP.NET.
  You can reenable them by uncommenting the line in the <HTTPHANDLERS>section
  of Machine.config that maps *.vsdisco to
  System.Web.Services.Discovery.DiscoveryRequestHandler and granting the
  ASPNET user account permission to read the IIS metabase. However,
  Microsoft is actively discouraging the use of VSDISCO files because they
  could represent a threat to Web server security.<br>
  <br>
  <b>Is it possible to prevent a browser from caching an ASPX page?</b><br>
  Just call SetNoStore on the HttpCachePolicy object exposed through the
  Response object's Cache property, as demonstrated here:<br>
  </font></p>
  <p><font face="Verdana" size="2" color="#000080">
  SetNoStore works by returning a Cache-Control: private, no-store header in
  the HTTP response. In this example, it prevents caching of a Web page that
  shows the current time.<br>
  <br>
  <b>What does AspCompat="true" mean and when should I use it?<br>
  </b>AspCompat is an aid in migrating ASP pages to ASPX pages. It defaults
  to false but should be set to true in any ASPX file that creates
  apartment-threaded COM objects--that is, COM objects registered
  ThreadingModel=Apartment. That includes all COM objects written with
  Visual Basic 6.0. AspCompat should also be set to true (regardless of
  threading model) if the page creates COM objects that access intrinsic ASP
  objects such as Request and Response. The following directive sets
  AspCompat to true:<br>
  <%@ Page AspCompat="true" %> <br>
  Setting AspCompat to true does two things. First, it makes intrinsic ASP
  objects available to the COM components by placing unmanaged wrappers
  around the equivalent ASP.NET objects. Second, it improves the performance
  of calls that the page places to apartment- threaded COM objects by
  ensuring that the page (actually, the thread that processes the request
  for the page) and the COM objects it creates share an apartment. AspCompat=&quot;true&quot;
  forces ASP.NET request threads into single-threaded apartments (STAs). If
  those threads create COM objects marked ThreadingModel=Apartment, then the
  objects are created in the same STAs as the threads that created them.
  Without AspCompat=&quot;true,&quot; request threads run in a multithreaded
  apartment (MTA) and each call to an STA-based COM object incurs a
  performance hit when it's marshaled across apartment boundaries.<br>
  Do not set AspCompat to true if your page uses no COM objects or if it
  uses COM objects that don't access ASP intrinsic objects and that are
  registered ThreadingModel=Free or ThreadingModel=Both.
  </font></td>
 </tr>
 <tr>
 <td width="100%" bgcolor="#33CC33" height="68"><font face="Verdana" size="2" color="#000080">
  <b>Can two different programming languages be mixed in a single ASMX file?
  </b><br>
  No. <br>
  <br>
  <b>What namespaces are imported by default in ASMX files? </b><br>
  The following namespaces are imported by default. Other namespaces must be
  imported manually.· System,
  System.Collections,System.ComponentModel,System.Data,
  System.Diagnostics,System.Web,System.Web.Services <br>
  How do I provide information to the Web Service when the information is
  required as a SOAP Header? <br>
  The key here is the Web Service proxy you created using wsdl.exe or
  through Visual Studio .NET's Add Web Reference menu option. If you happen
  to download a WSDL file for a Web Service that requires a SOAP header,
  .NET will create a SoapHeader class in the proxy source file. Using the
  previous example: <br>
  public class Service1 :
  System.Web.Services.Protocols.SoapHttpClientProtocol <br>
  { <br>
  public AuthToken AuthTokenValue; <br>
  <br>
  [System.Xml.Serialization.XmlRootAttribute(Namespace=&quot;http://tempuri.org/&quot;,
  IsNullable=false)] <br>
  public class AuthToken : SoapHeader { public string Token; }} <br>
  <br>
  In this case, when you create an instance of the proxy in your main
  application file, you'll also create an instance of the AuthToken class
  and assign the string: <br>
  Service1 objSvc = new Service1();<br>
  processingobjSvc.AuthTokenValue = new AuthToken();<br>
  objSvc.AuthTokenValue.Token = <ACTUAL token value>;<br>
  Web Servicestring strResult = objSvc.MyBillableWebMethod(); <br>
  </font></td>
 </tr>
</table>
```

