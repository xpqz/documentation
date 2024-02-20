




<h1 class="heading"><span class="name">OCXClass</span></h1>

[Parents](../ParentLists/OCXClass.htm) [Properties](../PropLists/OCXClass.htm) [Methods](../MethodLists/OCXClass.htm) [Events](../EventLists/OCXClass.htm)


Purpose: This object provides access to OLE (ActiveX) Controls.


**Description**


This object loads an OLE Control into memory and defines a new class of object associated with it. The name of the new class is the name specified by the left argument of `⎕WC`  You may create an instance of the newly defined class using the name you assigned to the OCXClass object as the Type property.



Note that you may not create an instance of OCXClass using `⎕NEW`.


Once you have defined a new OCXClass, the properties, events and methods it supports may be obtained from its [PropList](../a-z/proplist.md), [EventList](../a-z/eventlist.md) and [MethodList](../a-z/methodlist.md) properties. These are the properties, events and methods defined for the OLE control by its author.


The [QueueEvents](../a-z/queueevents.md) property determines how events reported by the ActiveX control are handled.


To find out how to use the OLE control, you must consult the appropriate documentation. However, a great deal of information about it can be obtained using the [GetPropertyInfo](../a-z/getpropertyinfo.md), [GetEventInfo](../a-z/geteventinfo.md), and [GetMethodInfo](../a-z/getmethodinfo.md) methods.


