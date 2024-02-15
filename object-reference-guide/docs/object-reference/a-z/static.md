




<h1 class="heading"><span class="name">Static</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object is primarily used to display graphics in a sub-window. |
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


The overall appearance of an empty Static object is controlled by the value of its [Style](./style.md) property which may be one of the following character vectors:



Note that the colours implied by the [Style](./style.md) are not "hard-coded" but are actually defined by the current Windows colour scheme as follows:

| Black | Window Border Colour |
| --- | ---  |
| Grey/Gray | Desktop Colour |
| White | Window Background Colour |


If the background colour of the Form is also set to the Window Background Colour, it follows that the [Style](./style.md)s `'WhiteFrame'` and `'WhiteBox'` make the Static itself invisible (against the background), although the contents of the Static will show. This makes the Static appear like an invisible clipping window.

| `'BlackFrame'` | `'BlackBox'` |
| --- | ---  |
| `'GreyFrame' or 'GrayFrame'` | `'GreyBox' or 'GrayBox'` |
| `'WhiteFrame'` | `'WhiteBox'` |


