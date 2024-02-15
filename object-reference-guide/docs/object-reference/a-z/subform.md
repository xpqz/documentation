




<h1 class="heading"><span class="name">SubForm</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object represents a window that is owned by and constrained         within another Form or an MDIClient . |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [ChooseFont](./choosefont.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |  |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) |
| [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) |
| [GetFocusObj](./getfocusobj.md) |  |  |
| Children | [Detach](./detach.md) [ChooseFont](./choosefont.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |  |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) |
| [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) |
| [GetFocusObj](./getfocusobj.md) |  |  |
| Properties | [Detach](./detach.md) [ChooseFont](./choosefont.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |  |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) |
| [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) |
| [GetFocusObj](./getfocusobj.md) |  |  |
| Methods | [Detach](./detach.md) [ChooseFont](./choosefont.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |  |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) |
| [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) |
| [GetFocusObj](./getfocusobj.md) |  |  |
| Events | [Detach](./detach.md) [ChooseFont](./choosefont.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |  |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) | [GetTextSize](./gettextsize.md) |
| [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) |
| [GetFocusObj](./getfocusobj.md) |  |  |


Description


If the SubForm is the child of a Form, it is
by default a simple featureless window that occupies the entire client area
(excluding standard [ToolBar](toolbar.md)s, StatusBars
and TabBars) of its parent.



The properties
that control its appearance, including [Sizeable](./sizeable.md),
[Moveable](./moveable.md), [SysMenu](./sysmenu.md),
[Border](./border.md), [MaxButton](./maxbutton.md) and [MinButton](./minbutton.md), all default to 0. The [EdgeStyle](./edgestyle.md) property also defaults to `'None'`, so the
background of the SubForm defaults to the Window Background colour.


If the SubForm is the child of an MDIClient,
its default appearance is the same as for a top-level Form.
By default its size is 25% of its parent client area and it is positioned in the
centre of its parent object.


The [Posn](./posn.md) property specifies the location of
the internal top-left corner of the SubForm relative to its parent. If
the SubForm has a title bar, border, or a 3-dimensional shadow, you must allow
sufficient space for these components. Similarly, the [Size](./size.md) property specifies the internal size of the SubForm excluding the title bar and
border.


A SubForm is constrained so that it cannot be moved outside its parent. In
all other respects it behaves in a similar manner to a Form object. See Form object and the descriptions of
its properties for further details.


