




<h1 class="heading"><span class="name">OLEServer</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The OLEServer object is used to establish a namespace as an OLE Server         object that can be used by an OLE Automation client. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [OLERegister](./oleregister.md) [OLEUnregister](./oleunregister.md) [SetFnInfo](./setfninfo.md) [SetVarInfo](./setvarinfo.md) [SetEventInfo](./seteventinfo.md) | [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) | [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) |
| [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| Children | [Detach](./detach.md) [OLERegister](./oleregister.md) [OLEUnregister](./oleunregister.md) [SetFnInfo](./setfninfo.md) [SetVarInfo](./setvarinfo.md) [SetEventInfo](./seteventinfo.md) | [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) | [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) |
| [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| Properties | [Detach](./detach.md) [OLERegister](./oleregister.md) [OLEUnregister](./oleunregister.md) [SetFnInfo](./setfninfo.md) [SetVarInfo](./setvarinfo.md) [SetEventInfo](./seteventinfo.md) | [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) | [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) |
| [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| Methods | [Detach](./detach.md) [OLERegister](./oleregister.md) [OLEUnregister](./oleunregister.md) [SetFnInfo](./setfninfo.md) [SetVarInfo](./setvarinfo.md) [SetEventInfo](./seteventinfo.md) | [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) | [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) |
| [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| Events | [Detach](./detach.md) [OLERegister](./oleregister.md) [OLEUnregister](./oleunregister.md) [SetFnInfo](./setfninfo.md) [SetVarInfo](./setvarinfo.md) [SetEventInfo](./seteventinfo.md) | [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) | [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |
| [Detach](./detach.md) | [OLERegister](./oleregister.md) | [OLEUnregister](./oleunregister.md) |
| [SetFnInfo](./setfninfo.md) | [SetVarInfo](./setvarinfo.md) | [SetEventInfo](./seteventinfo.md) |


Description


The OLEServer object allows you to export an APL namespace so that its
functions and variables become directly accessible to an OLE Automation client
application such as Microsoft Visual Basic or Microsoft Excel.



An OLEServer may be saved as an *out-of-process* OLE server (in a
workspace) or as an *in-process* OLE server (in a DLL). See *Interface
Guide* for details.


When you create an OLEServer object, APL allocates various OLE attributes to
it. For example, the CLSID, which uniquely identifies the object, is assigned at
this stage. However, the object is not actually *registered* until you
execute )SAVE.


Registration involves updating the Windows registry with information about
the object itself, such as its name, the command required to obtain it and so
forth. Registration also records information about all of the functions and
variables that your object exposes. Registration is therefore a non-trivial
operation and should be delayed until the point when you are ready to test your
OLEServer.


You may create an empty OLEServer object and then define functions and
variables within it. Alternatively, you may convert an existing namespace which
is already populated with functions and variables. The latter method is
recommended as it implies less registry activity during the development of the
object.


The [ExportedFns](./exportedfns.md) and [ExportedVars](./exportedvars.md) properties specify the names of the functions and variables that will be exposed
by the object to OLE clients.


The [RunMode](./runmode.md) property is a character
vector that specifies how the object serves multiple clients. It may be `'MultiUse'` (the default), `'SingleUse'`, or `'RunningObject'`.


The [ShowSession](./showsession.md) property is either 0
(the default) or 1 and specifies whether or not the APL Session window is
displayed when the first instance of the OLEServer is created.


[RunMode](./runmode.md) and [ShowSession](./showsession.md) apply only to *out-of-process* OLEServers.

