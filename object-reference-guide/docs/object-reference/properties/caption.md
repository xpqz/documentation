



<h1 class="heading"><span class="name">Caption</span></h1>

Applies To

| Applies To: | [BrowseBox](../a-z/browsebox.md) [Button](../a-z/button.md) [ColorButton](../a-z/colorbutton.md) [CoolBand](../a-z/coolband.md) [FileBox](../a-z/filebox.md) [Form](../a-z/form.md) [Group](../a-z/group.md) [HTMLRenderer](../a-z/htmlrenderer.md) [Label](../a-z/label.md) [Menu](../a-z/menu.md) [MenuItem](../a-z/menuitem.md) [MsgBox](../a-z/msgbox.md) [PropertyPage](../a-z/propertypage.md) [PropertySheet](../a-z/propertysheet.md) [Root](../a-z/root.md) [StatusField](../a-z/statusfield.md) [SubForm](../a-z/subform.md) [TabBtn](../a-z/tabbtn.md) [TabButton](../a-z/tabbutton.md) [ToolButton](../a-z/toolbutton.md) | [BrowseBox](../a-z/browsebox.md) | [Button](../a-z/button.md) | [ColorButton](../a-z/colorbutton.md) | [CoolBand](../a-z/coolband.md) | [FileBox](../a-z/filebox.md) | [Form](../a-z/form.md) | [Group](../a-z/group.md) | [HTMLRenderer](../a-z/htmlrenderer.md) | [Label](../a-z/label.md) | [Menu](../a-z/menu.md) | [MenuItem](../a-z/menuitem.md) | [MsgBox](../a-z/msgbox.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [Root](../a-z/root.md) | [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBtn](../a-z/tabbtn.md) | [TabButton](../a-z/tabbutton.md) | [ToolButton](../a-z/toolbutton.md) |  |
| --- | --- | ---  |
| [BrowseBox](../a-z/browsebox.md) | [Button](../a-z/button.md) | [ColorButton](../a-z/colorbutton.md) |
| [CoolBand](../a-z/coolband.md) | [FileBox](../a-z/filebox.md) | [Form](../a-z/form.md) |
| [Group](../a-z/group.md) | [HTMLRenderer](../a-z/htmlrenderer.md) | [Label](../a-z/label.md) |
| [Menu](../a-z/menu.md) | [MenuItem](../a-z/menuitem.md) | [MsgBox](../a-z/msgbox.md) |
| [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [Root](../a-z/root.md) |
| [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBtn](../a-z/tabbtn.md) |
| [TabButton](../a-z/tabbutton.md) | [ToolButton](../a-z/toolbutton.md) |  |


Description


The Caption property is a character vector specifying fixed text associated with the object. For example, Caption defines the label on a [Button](../a-z/button.md), the title of a [Form](../a-z/form.md), [SubForm](../a-z/subform.md) or [MsgBox](../a-z/msgbox.md), the heading in a [Group](../a-z/group.md), and the text of a [Menu](../a-z/menu.md) or a [MenuItem](../a-z/menuitem.md).


For the [Root](../a-z/root.md) object, Caption specifies the text displayed when Alt+Tab is used to switch to the Dyalog APL/W application. It may be used in conjunction with the [IconObj](../a-z/iconobj.md) property which specifies the name of an [Icon](../a-z/icon.md) object to be displayed alongside this text.


Its default value is an empty vector.


For a [Button](../a-z/button.md) or [Label](../a-z/label.md), if the Caption property  contains one or more linefeed characters (`⎕UCS 10`) the text is top-left justified or, for a [Button](../a-z/button.md) with [Style](../a-z/style.md)`'Push'`, centre-justifed ;  and automatically wraps on white-space characters (such as space and tab) to fit in the width provided.


For controls that support this feature, a single ampersand (&) is used to designate that the following character (if present) is an access key or an accelerator key and that character is underlined. The ampersand is not itself displayed. To negate this feature and cause an ampersand to be displayed, it is necessary to specify "&&".


