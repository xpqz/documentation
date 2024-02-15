




<h1 class="heading"><span class="name">Dockable</span></h1>
| Applies To: | [CoolBand](../a-z/coolband.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) | [ToolControl](../a-z/toolcontrol.md) |
| --- | --- | --- | --- | ---  |

| Applies To: | [CoolBand](../a-z/coolband.md) [Form](../a-z/form.md) [SubForm](../a-z/subform.md) [ToolControl](../a-z/toolcontrol.md) | [CoolBand](../a-z/coolband.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) | [ToolControl](../a-z/toolcontrol.md) |  |  |
| --- | --- | ---  |
| [CoolBand](../a-z/coolband.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) |
| [ToolControl](../a-z/toolcontrol.md) |  |  |


Description


The Dockable property specifies whether or not an object may be docked or undocked.



Dockable is a character vector containing `'Never'` (the default), `'Always'` or `'Disabled'`.


If Dockable is `'Never'`, the object may not be docked or undocked by the user, and the docking menu items are not present in the object's context menu. This is the default.


If Dockable is `'Always'`, the object may be docked or undocked by the user, and the docking menu items are present in the object's context menu.


If Dockable is `'Disabled'`, the object may not currently be docked or undocked by the user, but the docking menu items are present in the object's context menu.


Note that by default, the user may switch between Dockable `'Always'` and `'Disabled'` by toggling the *Dockable* menu item. If you want to exercise full control over this property, you may implement your own context menu (see [ContextMenu Event](../a-z/contextmenu.md))


