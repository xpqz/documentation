




<h1 class="heading"><span class="name">SetVarInfo</span></h1>

Applies To: [ActiveXControl](./activexcontrol.md) [OLEServer](./oleserver.md)


**Description**


This method is used to describe an APL variable that is to be exported as a property of an [ActiveXControl](./activexcontrol.md) or [OLEServer](./oleserver.md) object.


The argument to SetVarInfo is a 2 or 3-element array as follows:


*Variable info* is either a simple character vector that specifies the
[COM data type](../Miscellaneous/COM data types.htm) of the variable, or a 2-element vector of character vectors whose first element specifies a help string and whose second element specifies the [COM data type](../Miscellaneous/COM data types.htm).


*Help ID* is an optional integer value that identifies the help context id within the help file associated with the HelpFile property of the ActiveXControl object. The value `¯1` means that no help is provided. APL stores this information in the registry from where it may be retrieved by the host application.



