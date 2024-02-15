




<h1 class="heading"><span class="name">Group</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object is used to group a related set of controls together         visually, and to impose "radio-button" behaviour. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) | [ChooseFont](./choosefont.md) |  |  |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [ChooseFont](./choosefont.md) |  |  |
| Children | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) | [ChooseFont](./choosefont.md) |  |  |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [ChooseFont](./choosefont.md) |  |  |
| Properties | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) | [ChooseFont](./choosefont.md) |  |  |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [ChooseFont](./choosefont.md) |  |  |
| Methods | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) | [ChooseFont](./choosefont.md) |  |  |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [ChooseFont](./choosefont.md) |  |  |
| Events | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) | [ChooseFont](./choosefont.md) |  |  |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [ChooseFont](./choosefont.md) |  |  |


Description


A Group is displayed as an empty box with a border around it whose appearance
is defined by the [EdgeStyle](./edgestyle.md) property. The
[Caption](./caption.md) property defines a string of text
that is displayed in the top left border. The default value is an empty vector.



A Group will be resized if its parent Form or
Group is resized. It can also be resized directly by the user if its [Sizeable](./sizeable.md) property is set to 1. By default, when a Group is resized, it automatically
adjusts the size and position of its children to maintain the same proportions
within it as before. The resizing of a Group and its children can be controlled
using the [AutoConf](./autoconf.md) property or by enabling
the [Configure](./configure.md) event (31).


