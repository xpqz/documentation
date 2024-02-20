




<h1 class="heading"><span class="name">ActiveXContainer</span></h1>

[Parents](../ParentLists/ActiveXContainer.htm) [Properties](../PropLists/ActiveXContainer.htm) [Methods](../MethodLists/ActiveXContainer.htm) [Events](../EventLists/ActiveXContainer.htm)


Purpose: The ActiveXContainer object represents the application that is currently hosting an instance of an ActiveXControl object.


**Description**


An ActiveXContainer is used to represent the host application that is hosting an [ActiveXControl](../a-z/activexcontrol.md) object, and provides access to its ambient properties such as font, and colour.



An ActiveXContainer object is created using the [Container](../a-z/container.md) property of the [ActiveXControl](../a-z/activexcontrol.md) object.


For example, the following expression, executed within an [ActiveXControl](../a-z/activexcontrol.md) instance creates an ActiveXContainer named `'CONT'`
```apl
      'CONT' ⎕NS ⎕WG'Container'
```


The ambient properties of the host application are reported by the [FontObj](../a-z/fontobj.md), [BCol](../a-z/fcol.md) and [FCol](../a-z/bcol.md) properties which are all read-only.


The ActiveXContainer object supports the [AmbientChanged](../a-z/ambientchanged.md) event which is reported when any of the ambient properties change. This event allows the ActiveXContainer to react to such changes.


