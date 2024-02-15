



<h1 class="heading"><span class="name">Caption</span></h1>

Applies To

| Applies To: | [BrowseBox](./browsebox.md) [Button](./button.md) [ColorButton](./colorbutton.md) [CoolBand](./coolband.md) [FileBox](./filebox.md) [Form](./form.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [Label](./label.md) [Menu](./menu.md) [MenuItem](./menuitem.md) [MsgBox](./msgbox.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [Root](./root.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBtn](./tabbtn.md) [TabButton](./tabbutton.md) [ToolButton](./toolbutton.md) | [BrowseBox](./browsebox.md) | [Button](./button.md) | [ColorButton](./colorbutton.md) | [CoolBand](./coolband.md) | [FileBox](./filebox.md) | [Form](./form.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Label](./label.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) | [MsgBox](./msgbox.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [Root](./root.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBtn](./tabbtn.md) | [TabButton](./tabbutton.md) | [ToolButton](./toolbutton.md) |  |
| --- | --- | ---  |
| [BrowseBox](./browsebox.md) | [Button](./button.md) | [ColorButton](./colorbutton.md) |
| [CoolBand](./coolband.md) | [FileBox](./filebox.md) | [Form](./form.md) |
| [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Label](./label.md) |
| [Menu](./menu.md) | [MenuItem](./menuitem.md) | [MsgBox](./msgbox.md) |
| [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [Root](./root.md) |
| [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBtn](./tabbtn.md) |
| [TabButton](./tabbutton.md) | [ToolButton](./toolbutton.md) |  |


Description


The Caption property is a character vector specifying fixed text associated with the object. For example, Caption defines the label on a [Button](./button.md), the title of a [Form](./form.md), [SubForm](./subform.md) or [MsgBox](./msgbox.md), the heading in a [Group](./group.md), and the text of a [Menu](./menu.md) or a [MenuItem](./menuitem.md).


For the [Root](./root.md) object, Caption specifies the text displayed when Alt+Tab is used to switch to the Dyalog APL/W application. It may be used in conjunction with the [IconObj](iconobj.md) property which specifies the name of an [Icon](./icon.md) object to be displayed alongside this text.


Its default value is an empty vector.


For a [Button](./button.md) or [Label](./label.md), if the Caption property  contains one or more linefeed characters (`⎕UCS 10`) the text is top-left justified or, for a [Button](./button.md) with Style`'Push'`, centre-justifed ;  and automatically wraps on white-space characters (such as space and tab) to fit in the width provided.


For controls that support this feature, a single ampersand (&) is used to designate that the following character (if present) is an access key or an accelerator key and that character is underlined. The ampersand is not itself displayed. To negate this feature and cause an ampersand to be displayed, it is necessary to specify "&&".


