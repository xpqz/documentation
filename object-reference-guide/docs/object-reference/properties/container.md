




<h1 class="heading"><span class="name">Container</span></h1>
| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) |
| --- | ---  |

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) | [ActiveXControl](../a-z/activexcontrol.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) |  |  |


Description


The Container property is a read-only property whose value is the `⎕OR` of an ActiveXContainer object that represents the *ActiveX Site* object of the application that is hosting the [ActiveXControl](../a-z/activexcontrol.md).


The value of Container may be converted to a namespace using `⎕NS` or `⎕WC`.


The resulting object may then be used to obtain the values of ambient properties, or to access methods exposed by the host application via OLE interfaces. See [OLEQueryInterface](../a-z/olequeryinterface.md).



