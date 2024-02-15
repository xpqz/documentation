




<h1 class="heading"><span class="name">Style</span></h1>

Applies To

| Applies To: | [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [FileBox](../a-z/filebox.md) [Icon](../a-z/icon.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Locator](../a-z/locator.md) [Marker](../a-z/marker.md) [MenuItem](../a-z/menuitem.md) [MsgBox](../a-z/msgbox.md) [ProgressBar](../a-z/progressbar.md) [PropertySheet](../a-z/propertysheet.md) [Separator](../a-z/separator.md) [Splitter](../a-z/splitter.md) [Static](../a-z/static.md) [StatusField](../a-z/statusfield.md) [TabControl](../a-z/tabcontrol.md) [TCPSocket](../a-z/tcpsocket.md) [ToolButton](../a-z/toolbutton.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [FileBox](../a-z/filebox.md) | [Icon](../a-z/icon.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Locator](../a-z/locator.md) | [Marker](../a-z/marker.md) | [MenuItem](../a-z/menuitem.md) | [MsgBox](../a-z/msgbox.md) | [ProgressBar](../a-z/progressbar.md) | [PropertySheet](../a-z/propertysheet.md) | [Separator](../a-z/separator.md) | [Splitter](../a-z/splitter.md) | [Static](../a-z/static.md) | [StatusField](../a-z/statusfield.md) | [TabControl](../a-z/tabcontrol.md) | [TCPSocket](../a-z/tcpsocket.md) | [ToolButton](../a-z/toolbutton.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) |  |
| --- | --- | ---  |
| [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [FileBox](../a-z/filebox.md) | [Icon](../a-z/icon.md) |
| [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Locator](../a-z/locator.md) |
| [Marker](../a-z/marker.md) | [MenuItem](../a-z/menuitem.md) | [MsgBox](../a-z/msgbox.md) |
| [ProgressBar](../a-z/progressbar.md) | [PropertySheet](../a-z/propertysheet.md) | [Separator](../a-z/separator.md) |
| [Splitter](../a-z/splitter.md) | [Static](../a-z/static.md) | [StatusField](../a-z/statusfield.md) |
| [TabControl](../a-z/tabcontrol.md) | [TCPSocket](../a-z/tcpsocket.md) | [ToolButton](../a-z/toolbutton.md) |
| [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) |  |


Description


This property determines a particular style of object within the general
category of [Type](../a-z/type.md).



It is a character vector whose value depends upon the type of object.


For a [Button](../a-z/button.md), Style may be `'Push'`,
`'Radio'`, `'Check'`, `'Toggle'`, `'CommandLink'` or `'Split'`.


`'Push'` specifies that the button
appears and behaves like a pushbutton (sometimes also called a command button).


`'Radio'` means that the button is
displayed as a small circle accompanied by a description. When the button is
selected, the circle is filled in. In a group of buttons with Style `'Radio'` that share the same parent, only one of them may be selected. This style of
button is generally known as a "radio-button" or an "option
button".


`'Check'` or `'Toggle'` means that the button is
displayed as a small box accompanied by a description. When the button is
selected a cross appears in the box. This style of button is known as a
"check-box".


`'CommandLink'` means that the button has an icon displayed to the left of its [Caption](../a-z/caption.md), the appearance of which is controlled by the  [Elevated](../a-z/elevated.md) property. 
Note that this feature only applies if  is enabled.


`'Split'` specifies a `'Push'` button with an additional drop-down button, similar to that provided by a [Combo](../a-z/combo.md) object. 
Note that this feature only applies if  is enabled.


For a [Calendar](../a-z/calendar.md) object, The Style property
may be either `'Single'` (the default) or `'Multi'`.
If Style is `'Single'`, the user may select
a single date. If Style is `'Multi`', the
user may select a contiguous range of dates.


For a [Combo](../a-z/combo.md) or [ComboEx](../a-z/comboex.md) object, Style may be `'Simple'` `'DropEdit'` or `'Drop'` (the default). `'Simple'` specifies a simple combo box in which the associated list box is displayed at
all times. The other two styles provide list boxes which "drop down"
when the user clicks on a symbol displayed to the right of the [Combo](../a-z/combo.md)'s
edit field. A `'DropEdit'` Style allows the
user to type (anything) in the edit field. A `'Drop'` Style forces the contents of the edit field to be either empty or
one of the choices specified by [Items](../a-z/items.md).


For a [DateTimePicker](../a-z/datetimepicker.md), Style may be
either `'Combo'` (the default) or `'UpDown'`.


For an [Edit](../a-z/edit.md) object, Style may be `'Single'` or `'Multi'`. If Style is `'Single'` the object displays only a single line of text and the user may not enter any
more lines. If the Style is `'Multi'` the
number of lines displayed is governed by the [Rows](../a-z/rows.md) or [Size](../a-z/size.md) property and the user may insert, add
or delete lines as desired.


For [FileBox](../a-z/filebox.md), [List](../a-z/list.md),
and [ListView](../a-z/listview.md) objects, Style may be `'Single'` or `'Multi'`. If the Style is `'Single'`only one file or item can be selected. If Style is `'Multi'`,
several files or items can be selected.


For an [Icon](../a-z/icon.md), Style may be `'Large'` (the default) or `'Small'` and specifies the
size of the icon (32x32 or 16x16) to be loaded from a file.


For a [Locator](../a-z/locator.md), Style may be `'Point'`,
`'Rect'` (the default), `'Line'` or `'Ellipse'`. It specifies the shape that
is drawn as the user moves the mouse.


For a [MenuItem](../a-z/menuitem.md), Style may be `'Check'` (the default) or `'Radio'`. The latter
specifies that within a contiguous block of such MenuItems, only one may have [Checked](../a-z/checked.md) set to 1. Setting [Checked](../a-z/checked.md) to 1 on any item
in that group automatically sets [Checked](../a-z/checked.md) to
0 on the others. A radio style [MenuItem](../a-z/menuitem.md) that
is checked has a small radio dot drawn to the left of its Caption.



For a [MsgBox](../a-z/msgbox.md), the Style property determines
the type of icon which is displayed in it. This is a character vector with one
of the following values:




For a [Static](../a-z/static.md) object, Style defines its
appearance, and may be one of:




A [StatusField](../a-z/statusfield.md) may be used to monitor
the state of a key on the keyboard. If so, its Style property determines the key
it monitors and may be one of the following:



For a [Splitter](../a-z/splitter.md), the Style property
specifies the orientation of the [Splitter](../a-z/splitter.md) and may be `'Vert'` (the default) or `'Horz'`.


For a [TabControl](../a-z/tabcontrol.md), the Style property
determines the appearance of its [TabButton](../a-z/tabbutton.md) children, and may be `'Tabs'` (the default),
`'Buttons'` or `'FlatButtons'`.


For a [TCPSocket](../a-z/tcpsocket.md), Style is a character
vector that specifies the type of data transmitted or received by the socket; it
may be `'Char'`, `'Raw'`,
or `'APL'`. The value APL is valid only if
the [SocketType](../a-z/sockettype.md) is '`Stream'`.


For a [ToolButton](../a-z/toolbutton.md), the Style property
specifies the behaviour of the button and may be `'Push'` (the default), `'Check'`, `'Radio'`,
`'DropDown'`, or `'Separator'`.


For a [ToolControl](../a-z/toolcontrol.md), the Style property
determines the appearance of its [ToolButton](../a-z/toolbutton.md) children and may be `'Buttons'`, `'FlatButtons'` (the default), `'List'` or `'FlatList'`.


For a [TrackBar](../a-z/trackbar.md), the Style property
determines the appearance and behaviour of the TrackBar and may be `'Standard'` (the default) or `'Selection'`.

| `'Msg'` | no icon (the default) |
| --- | ---  |
| `'Info'` | information message icon |
| `'Query'` | query (question) icon |
| `'Warn'` | warning icon |
| `'Error'` | critical error icon |

| `'BlackFrame'` | `'BlackBox'` |
| --- | ---  |
| `'GreyFrame' or 'GrayFrame'` | `'GreyBox' or 'GrayBox'` |
| `'WhiteFrame'` | `'WhiteBox'` |

| CapsLock | Monitors state of Caps Lock key |
| --- | ---  |
| ScrollLock | Monitors state of Scroll Lock key |
| NumLock | Monitors state of Num Lock key |
| KeyMode | Monitors the keyboard mode (APL/ASCII) |
| InsRep | Monitors the state of the Insert key |


