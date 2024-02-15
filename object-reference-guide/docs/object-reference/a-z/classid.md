




<h1 class="heading"><span class="name">ClassID</span></h1>

| Applies To: | [ActiveXControl](./activexcontrol.md) | [OCXClass](./ocxclass.md) | [OLEClient](./oleclient.md) | [OLEServer](./oleserver.md) |
| --- | --- | --- | --- | ---  |


**Description**


The ClassID property specifies the class identifier (usually abbreviated to CLSID) of an APL object that is used to represent a COM object. The CLSID is a globally unique identifier ([GUID](../Miscellaneous/Globally%20Unique%20Identifier%20GUID.htm)) that uniquely identifies the object.


When you create or recreate an ActiveXControl or [OLEServer](./oleserver.md) using `⎕WC`, you may specify ClassID. This allows you to re-use a value that was previously allocated to that control by the system. However, you should not specify any other value because that value could be allocated now or in the future to another object *on any other computer in the world*. Otherwise, a new ClassID is automatically allocated by the system.


Note that the CLSID is not actually recorded on your computer (in the registry) until you register it using `)SAVE` or *Make OCX*, or by executing the [OLERegister](./oleregister.md) method.



