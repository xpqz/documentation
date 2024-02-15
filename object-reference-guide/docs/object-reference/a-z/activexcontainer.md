




<h1 class="heading"><span class="name">ActiveXContainer</span></h1>
| Parents | Properties | Methods | Events |
| --- | --- | --- | ---  |

| Purpose: | The ActiveXContainer object represents the application that is currently hosting an instance of an ActiveXControl object. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [OLEQueryInterface](./olequeryinterface.md) | [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| Properties | [Detach](./detach.md) [OLEQueryInterface](./olequeryinterface.md) | [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| Methods | [Detach](./detach.md) [OLEQueryInterface](./olequeryinterface.md) | [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| Events | [Detach](./detach.md) [OLEQueryInterface](./olequeryinterface.md) | [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |
| [Detach](./detach.md) | [OLEQueryInterface](./olequeryinterface.md) |  |


Description


An ActiveXContainer is used to represent the host application that is hosting an ActiveXControl object, and provides access to its ambient properties such as font, and colour.



An ActiveXContainer object is created using the [Container](./container.md) property of the ActiveXControl object.


For example, the following expression, executed within an ActiveXControl instance creates an ActiveXContainer named `'CONT'`
```apl
      'CONT' ⎕NS ⎕WG'Container'
```


The ambient properties of the host application are reported by the [FontObj](./fontobj.md), [BCol](./fcol.md) and [FCol](./bcol.md) properties which are all read-only.


The ActiveXContainer object supports the [AmbientChanged](./ambientchanged.md) event which is reported when any of the ambient properties change. This event allows the ActiveXContainer to react to such changes.


