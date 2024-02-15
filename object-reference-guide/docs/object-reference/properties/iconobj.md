




<h1 class="heading"><span class="name">IconObj</span></h1>

Applies To

| Applies To: | [Form](../a-z/form.md) [HTMLRenderer](../a-z/htmlrenderer.md) [MDIClient](../a-z/mdiclient.md) [Root](../a-z/root.md) [SubForm](../a-z/subform.md) [SysTrayItem](../a-z/systrayitem.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) | [Form](../a-z/form.md) | [HTMLRenderer](../a-z/htmlrenderer.md) | [MDIClient](../a-z/mdiclient.md) | [Root](../a-z/root.md) | [SubForm](../a-z/subform.md) | [SysTrayItem](../a-z/systrayitem.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) |  |
| --- | --- | ---  |
| [Form](../a-z/form.md) | [HTMLRenderer](../a-z/htmlrenderer.md) | [MDIClient](../a-z/mdiclient.md) |
| [Root](../a-z/root.md) | [SubForm](../a-z/subform.md) | [SysTrayItem](../a-z/systrayitem.md) |
| [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) |  |


Description


This property is used to specify a *large* and *small* icon for a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), or for the [Root](../a-z/root.md) object which represents your application as a whole. Its value is either a single ref or character scalar or vector containing the name of, or ref to, an Icon object, or a 2-element vector of character vectors or refs that specifies 2 [Icon](../a-z/icon.md) objects.


If empty (the default value), the standard "Dyalog APL GUI" icon is used.


The large and small icons are supplied to the Operating System which uses them as and when is appropriate. Normally, the large icon is of size 32x32 and the small icon is 16x16. If you specify an icon of a different size, the Operating System will scale it as appropriate.


The icon associated with a [Form](../a-z/form.md) is displayed when the [Form](../a-z/form.md) is minimised. The icon associated with `'.'` is displayed when the user presses Alt+Tab to toggle between applications. In both cases, the text shown underneath or alongside the icon is defined by the [Caption](../a-z/caption.md) property.



