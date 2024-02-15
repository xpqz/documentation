




<h1 class="heading"><span class="name">MenuBar</span></h1>

| [Parents](../ParentLists/MenuBar.htm) | [Children](../ChildLists/MenuBar.htm) | [Properties](../PropLists/MenuBar.htm) | [Methods](../MethodLists/MenuBar.htm) | [Events](../EventLists/MenuBar.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Specifies a horizontal menu bar displayed at the top of a [Form](form.md) . |
| --- | ---  |


**Description**


Unless it is made invisible the MenuBar is always available to the user to initiate actions or to select options. A MenuBar has a fixed position and size.



It is possible to have more than one MenuBar associated with the same [Form](form.md) or [SubForm](subform.md), but only one of them should be [Visible](./visible.md) at any one time.


The following example illustrates how a menu structure can be built up from a MenuBar. For clarity, the example is indented, and the definition of the [Event](./event.md) property is omitted.
```apl
      'F'           ⎕WC 'Form' 'Menu Example'
      'F.M'         ⎕WC 'MenuBar'
      'F.M.FILE'    ⎕WC 'Menu' '&File'
      'F.M.MAT'     ⎕WC 'Menu' '&Materials'
      'F.M.MAT.B'   ⎕WC 'MenuItem' '&Brick'
      'F.M.MAT.C'   ⎕WC 'MenuItem' '&Concrete'
      'F.M.MAT.S'   ⎕WC 'MenuItem' '&Stone'
      'F.M.MAT.SEP' ⎕WC 'Separator'
      'F.M.MAT.W'   ⎕WC 'Menu'     '&Wood'
      'F.M.MAT.W.O' ⎕WC 'MenuItem' '&Oak'
      'F.M.MAT.W.T' ⎕WC 'MenuItem' '&Teak'
      'F.M.MAT.W.M' ⎕WC 'MenuItem' '&Mahogany'
```


Note that putting a [Separator](separator.md) (either [Style](./style.md)) in a MenuBar has the effect of breaking the bar vertically, i.e. the next [Menu](menu.md) or [MenuItem](menuitem.md) you add will appear on the left-hand side on the line below.


The [EdgeStyle](./edgestyle.md) property has no effect on the appearance of a MenuBar or of a direct child of a MenuBar. However, if you want the sub-menus to have a 3-dimensional appearance, you **must** set the [EdgeStyle](./edgestyle.md) property of the MenuBar to something other than `'None'`.


If the MenuBar is owned by a [Form](form.md) that is the parent of an [MDIClient](mdiclient.md), you can set the [MDIMenu](./mdimenu.md) property to the name of the [Menu](menu.md) you wish to nominate as the *window*  menu. This menu will automatically be updated with the [Caption](./caption.md)s of the child [SubForm](subform.md) and may be used to select the currently active one.


