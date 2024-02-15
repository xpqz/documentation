




<h1 class="heading"><span class="name">ColorButton</span></h1>
| Parents | Properties | Methods | Events |
| --- | --- | --- | ---  |

| Purpose: | The ColorButton object allows the user to select a colour. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Properties | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Methods | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Events | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |


Description


The ColorButton object displays a coloured box, with an optional drop down button. When the user clicks the ColorButton with the left mouse button, a colour selection drop-down appears below it, allowing the user to select a new colour.



The [CurrentColor](./currentcolor.md) property (default 0 0 0) is a 3-element integer vector that specifies and reports the RGB value of the currently selected colour.


The [DefaultColors](./defaultcolors.md) property is a nested matrix which specifies the RGB values of the colours shown in the colour selection box. The shape of [DefaultColors](./defaultcolors.md) determines the number of rows and columns in the colour selection drop-down. Each element of [DefaultColors](./defaultcolors.md) is a 3-element integer vector specifying an RGB colour value.


The [OtherButton](./otherbutton.md) property is Boolean and specifies whether or not the user can select a colour using the Windows colour selection dialog box.


If [OtherButton](./otherbutton.md) is 1 (the default), the final row of the colour selection drop-down contains a button labelled "Other…". If the user clicks this button, the standard Windows colour selection dialog box is displayed, allowing the user to select any colour that the computer can render.


If [OtherButton](./otherbutton.md) is 0, the button labelled "Other…" is not present and the user is restricted to the choice of colours provided by the [DefaultColors](./defaultcolors.md) property.


The [CustomColors](./customcolors.md) property is a 1-row, 16-column nested matrix which specifies the RGB values of the Colours displayed in the *Custom colors* section of the Windows colour selection dialog box. Each element of [CustomColors](./customcolors.md) is a 3-element integer vector specifying an RGB colour value.


The [ShowDropDown](./showdropdown.md) property is Boolean (default 1) and specifies whether or not a drop-down button is displayed in the ColorButton object.


When the user clicks a ColorButton with the left mouse button, the object generates a [DropDown](./dropdown.md) event just before it displays the colour selection drop-down. This event may be used to set the [DefaultColors](./defaultcolors.md) and/or [CustomColors](./customcolors.md) properties dynamically.


When the user selects a new colour, the ColorButton generates a [ColorChange](./colorchange.md) event.


Note that Pocket PC 2002 colour selection dialog box does not provide the facility to select *custom colours*, so this functionality is not available in PocketAPL.


