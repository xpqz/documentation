




<h1 class="heading"><span class="name">OLEAddEventSink</span></h1>
| Applies To: | [OCXClass](./ocxclass.md) | [OLEClient](./oleclient.md) |
| --- | --- | ---  |

| Applies To: | [OCXClass](./ocxclass.md) [OLEClient](./oleclient.md) | [OCXClass](./ocxclass.md) | [OLEClient](./oleclient.md) |  |
| --- | --- | ---  |
| [OCXClass](./ocxclass.md) | [OLEClient](./oleclient.md) |  |


Description


This method connects a named event sink to a COM object and adds the events defined by that event sink to the [EventList](./eventlist.md) property of the associated namespace.


The argument to OLEAddEventSink is a single item as follows:

| `[1]` | Event sink name | character vector |
| --- | --- | ---  |


The result is a number that represents the handle of the event sink. This may be subsequently required.



