




<h1 class="heading"><span class="name">ClassID</span></h1>
| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) | [OCXClass](../a-z/ocxclass.md) | [OLEClient](../a-z/oleclient.md) | [OLEServer](../a-z/oleserver.md) |
| --- | --- | --- | --- | ---  |

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [OCXClass](../a-z/ocxclass.md) [OLEClient](../a-z/oleclient.md) [OLEServer](../a-z/oleserver.md) | [ActiveXControl](../a-z/activexcontrol.md) | [OCXClass](../a-z/ocxclass.md) | [OLEClient](../a-z/oleclient.md) | [OLEServer](../a-z/oleserver.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [OCXClass](../a-z/ocxclass.md) | [OLEClient](../a-z/oleclient.md) |
| [OLEServer](../a-z/oleserver.md) |  |  |


Description


The ClassID property specifies the class identifier (usually abbreviated to CLSID) of an APL object that is used to represent a COM object. The CLSID is a globally unique identifier (GUID) that uniquely identifies the object.


When you create or recreate an ActiveXControl or [OLEServer](../a-z/oleserver.md) using `⎕WC`, you may specify ClassID. This allows you to re-use a value that was previously allocated to that control by the system. However, you should not specify any other value because that value could be allocated now or in the future to another object *on any other computer in the world*. Otherwise, a new ClassID is automatically allocated by the system.


Note that the CLSID is not actually recorded on your computer (in the registry) until you register it using `)SAVE` or *Make OCX*, or by executing the [OLERegister](../a-z/oleregister.md) method.



