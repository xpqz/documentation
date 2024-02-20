




<h1 class="heading"><span class="name">OLEClient</span></h1>

[Parents](../ParentLists/OLEClient.htm) [Children](../ChildLists/OLEClient.htm) [Properties](../PropLists/OLEClient.htm) [Methods](../MethodLists/OLEClient.htm) [Events](../EventLists/OLEClient.htm)


Purpose: The OLEClient object provides access to an OLE Automation Server


**Description**


The OLEClient object allows you to control OLE Servers, which may be written
in a variety of different programming languages, including Dyalog APL itself.



The [ClassName](../a-z/classname.md) property specifies the
name of the OLE object to which the new object named by the left argument of `⎕WC` is to be connected. A list of all the OLE Server objects installed on your
system may be obtained from the OLEServers property of Root. [ClassName](../a-z/classname.md) may only be specified by `⎕WC`.


Alternatively, the OLE object may be identified by the [ClassID](../a-z/classid.md) property.


The AutoBrowse property and Browse method are no longer relevant and are
ignored. They are retained only for backwards compatibility with previous
versions of Dyalog APL.


Note that the PropList and MethodList properties of an OLEClient instance
contain the names of the properties and methods exposed by the corresponding OLE
Object in addition to the generic properties and methods of the OLEClient class.


If you call an OLE method with an invalid parameter, set a read-only
property, or assign it an invalid value, the [LastError](../a-z/lasterror.md) property of the OLEClient and [Root](../a-z/root.md) objects will
contain error information generated by OLE.

