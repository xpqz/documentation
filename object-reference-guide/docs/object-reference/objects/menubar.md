




<h1 class="heading"><span class="name">MenuBar</span></h1>

| [Parents](../ParentLists/MenuBar.htm) | [Children](../ChildLists/MenuBar.htm) | [Properties](../PropLists/MenuBar.htm) | [Methods](../MethodLists/MenuBar.htm) | [Events](../EventLists/MenuBar.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Specifies a horizontal menu bar displayed at the top of a [Form](../a-z/form.md) . |
| --- | ---  |


**Description**


Unless it is made invisible the MenuBar is always available to the user to initiate actions or to select options. A MenuBar has a fixed position and size.



It is possible to have more than one MenuBar associated with the same [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), but only one of them should be [Visible](../a-z/visible.md) at any one time.


The following example illustrates how a menu structure can be built up from a MenuBar. For clarity, the example is indented, and the definition of the [Event](../a-z/event.md) property is omitted.
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


Note that putting a [Separator](../a-z/separator.md) (either [Style](../a-z/style.md)) in a MenuBar has the effect of breaking the bar vertically, i.e. the next [Menu](../a-z/menu.md) or [MenuItem](../a-z/menuitem.md) you add will appear on the left-hand side on the line below.


The [EdgeStyle](../a-z/edgestyle.md) property has no effect on the appearance of a MenuBar or of a direct child of a MenuBar. However, if you want the sub-menus to have a 3-dimensional appearance, you **must** set the [EdgeStyle](../a-z/edgestyle.md) property of the MenuBar to something other than `'None'`.


If the MenuBar is owned by a [Form](../a-z/form.md) that is the parent of an [MDIClient](../a-z/mdiclient.md), you can set the [MDIMenu](../a-z/mdimenu.md) property to the name of the [Menu](../a-z/menu.md) you wish to nominate as the *window*  menu. This menu will automatically be updated with the [Caption](../a-z/caption.md)s of the child [SubForm](../a-z/subform.md) and may be used to select the currently active one.


