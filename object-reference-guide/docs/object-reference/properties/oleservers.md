




<h1 class="heading"><span class="name">OLEServers</span></h1>
| Applies To: | [Root](../a-z/root.md) |
| --- | ---  |

| Applies To: | [Root](../a-z/root.md) | [Root](../a-z/root.md) |  |  |
| --- | --- | ---  |
| [Root](../a-z/root.md) |  |  |


Description


The OLEServers property is a read-only property that reports the names and CLSIDs of all the OLE Automation servers installed on your computer. This information comes from the Windows registry.


Its value is a nested vector with one element per OLE Server.


Each element is a vector of 2-element character vectors. The first is the name of the OLE Server; the second is its class identifier or CLSID which is a type of GUID.



