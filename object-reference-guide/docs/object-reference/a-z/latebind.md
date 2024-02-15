




<h1 class="heading"><span class="name">LateBind</span></h1>
| Applies To: | [OLEClient](./oleclient.md) | [OLEServer](./oleserver.md) |
| --- | --- | ---  |

| Applies To: | [OLEClient](./oleclient.md) [OLEServer](./oleserver.md) | [OLEClient](./oleclient.md) | [OLEServer](./oleserver.md) |  |
| --- | --- | ---  |
| [OLEClient](./oleclient.md) | [OLEServer](./oleserver.md) |  |


Description





LateBind is a Boolean property that determines whether or not the Type Information is read when an [OLEClient](./oleclient.md) object is instantiated, or when an [OLEServer](./oleserver.md) references a COM object. It must be set when the [OLEClient](./oleclient.md) or [OLEServer](./oleserver.md) object is created and cannot subsequently be changed.


If LateBind is 0 (the default) the Type information is obtained, in its entirety, when the [OLEClient](./oleclient.md) object is instantiated or when an [OLEServer](./oleserver.md) processes a reference to an external COM object.


If LateBind is 1, APL postpones the calls to obtain Type Information until a particular property, method or event of the COM object is referenced; and then only for that particular member.



