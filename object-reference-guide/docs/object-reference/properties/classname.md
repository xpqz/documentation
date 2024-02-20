




<h1 class="heading"><span class="name">ClassName</span></h1>

Applies To: [ActiveXControl](../a-z/activexcontrol.md) [OCXClass](../a-z/ocxclass.md) [OLEClient](../a-z/oleclient.md) [OLEServer](../a-z/oleserver.md)


**Description**


For an [OLEClient](../a-z/oleclient.md), the ClassName property specifies the name of the OLE object to which an [OLEClient](../a-z/oleclient.md) object named by the left argument of `⎕WC` is to be connected.
Similarly, for a [NetControl](../Objects/NetControl.htm) the ClassName property specifies the name of the .NET class to be instantiated.
Note that ClassName is mandatory for `⎕WC` and may not subsequently be changed using `⎕WS`.


For an [ActiveXControl](../a-z/activexcontrol.md) or [OLEServer](../a-z/oleserver.md), ClassName specifies the external name with which the object is registered, and by which it is referenced by other applications.


For an [ActiveXControl](../a-z/activexcontrol.md), the external name is  "Dyalog xxx Control, where xxx is the value of the ClassName property, or, if ClassName is not specified, the name of the [ActiveXControl](../a-z/activexcontrol.md) namespace.


For an [OLEServer](../a-z/oleserver.md), the external name is "Dyalog.xxx" where xxx is derived in the same way.


For a NetControl, the external name is the name of the .NET class which must be expressed relative to a corresponding element of `⎕USING`.
For example, to load one of the standard .NET controls:
```apl
      ⎕USING,←⊂'System.Windows.Forms,system.windows.forms.dll'
```



