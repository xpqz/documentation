




<h1 class="heading"><span class="name">Form</span></h1>

[Parents](../ParentLists/Form.htm) [Children](../ChildLists/Form.htm) [Properties](../PropLists/Form.htm) [Methods](../MethodLists/Form.htm) [Events](../EventLists/Form.htm)


Purpose: This is a top-level window used to contain other objects (controls).


**Description**



The [Posn](./posn.md) property specifies the location of
the **internal** top-left corner of the window relative to the top-left
corner of the screen. If the window has a title bar and/or border, you must
allow sufficient space for them. Similarly, the [Size](./size.md) property specifies the internal size of the window excluding the title bar and
border. The default for [Size](./size.md) is 50% of the
screen height and width. The default for [Posn](./posn.md) places the Form in the middle of the screen.


Normally, a Form has a title bar, a system menu box, a border and maximise
and minimise buttons. To disable the System Menu box, set [SysMenu](./sysmenu.md) to 0. To disable one or both of the maximise/minimise buttons, set [MaxButton](./maxbutton.md) and/or [MinButton](./minbutton.md) to 0.


The [HelpButton](./helpbutton.md) property specifies
that a Question (?) button appears in the title bar of the Form. However, this
does not apply if the Form has a maximise or minimise button which both take
precedence. The user may obtain help by clicking on the Question (?) button and
then on a control in the Form. It is up to you to provide the help by responding
to the [Help](./help.md) event on the control.


By default, a Form may be moved and resized using the mouse. These actions
are achieved by dragging on the title bar and border respectively. It follows
that a Form that is [Moveable ](./moveable.md)**must** have a title bar, and one that is [Sizeable](./sizeable.md) **must** have a border, regardless of the value of other properties. Also, if
you specify any of [SysMenu](./sysmenu.md), [MaxButton](./maxbutton.md) or [MinButton](./minbutton.md), the window must have a
title bar in which to place these controls. A title bar itself requires a
border. To obtain a window without a title bar, you must therefore set [Moveable](./moveable.md),
[SysMenu](./sysmenu.md), [MaxButton](./maxbutton.md) and [MinButton](./minbutton.md) to 0. Note that setting [Caption](./caption.md) does **not** force a title bar on the window.


If [Sizeable](./sizeable.md) is 1, the window will have
a double-line border, regardless of the values of other properties. If [Sizeable](./sizeable.md) is 0, and any one or more of [Moveable](./moveable.md), [SysMenu](./sysmenu.md),
[MaxButton](./maxbutton.md), [MinButton](./minbutton.md) or [Border](./border.md) is 1, the window will have a
1-pixel border. Only if all these properties are 0 will the window be
borderless. To obtain a dialog box that may only be moved or closed, set [Border](./border.md) to 2.


Note that the default value for [Caption](./caption.md) is an empty character vector which results in a blank title.


To obtain a standard dialog box with 3-dimensional appearance, create a Form
with [Border](./border.md) set to 2 and [EdgeStyle](./edgestyle.md) set to `'Dialog'`, for example:
```apl
  'F' ⎕WC 'Form' 'Dialog Box' ('EdgeStyle' 'Dialog')('Border' 2)
```


The [State](./state.md) property has the value 0 if the
window is currently displayed in its "normal" state, 1 if it is
currently displayed as an icon, and 2 if it is currently maximised and displayed
full-screen. This property does not just report the current state, but can be
used to set the state under program control.


The [VScroll](./vscroll.md) and [HScroll](./hscroll.md) properties determine whether or not a Form has a vertical and horizontal
scrollbar respectively. These properties are set to `¯1`to obtain a scrollbar. Their default value is 0 (no scrollbar). [VScroll](./vscroll.md) and [HScroll](./hscroll.md) may only be set when the object is created and may not subsequently be changed. The [Range](./range.md) property is a 2-element vector that specifies the maximum value for the vertical
and horizontal scrollbars respectively. The [PageSize](./pagesize.md) property is a 2-element vector that specifies the sizes of the thumbs in each scrollbar. The [Step](./step.md) property is a 4-element vector that specifies the sizes of the small and large
change. Its first two elements refer to the vertical scrollbar, elements 3 and 4
refer to the horizontal scrollbar. The [Thumb](./thumb.md) property is a 2-element vector that both reports and sets the position of the
thumb in the vertical and horizontal scrollbars respectively. When the user
attempts to move the thumb in one of the scrollbars, the Form generates a [VScroll](./vscroll.md) or [HScroll](./hscroll.md) event.


[VScroll](./vscroll.md) and [HScroll](./hscroll.md) cannot be changed using [`⎕WS`](../../Language/System Functions/ws.htm).
However, you can make a scrollbar disappear by setting the corresponding element
of [Range](./range.md) to 1, thus allowing you to
dynamically switch the scrollbar off and on. Note however that doing so will
change the size of the Form.


Setting the [FontObj](./fontobj.md) property on a Form
does not affect the text in its title bar. However, the value of [FontObj](./fontobj.md) will (unless over-ridden) be inherited by all of the objects within the Form.


The background of the Form may be coloured using [BCol](./bcol.md).
The default value for [BCol](./bcol.md) is the Windows
Button Face colour unless [EdgeStyle](./edgestyle.md) is
set to `'None'` or `'Default'` in which case it is the Windows background colour. Alternatively, the background
of a Form can be defined using a [Bitmap](bitmap.md) or [Metafile](metafile.md) object whose name is defined by the [Picture](./picture.md) property. A [Metafile](metafile.md) is automatically scaled
to fit the Form. A [Bitmap](bitmap.md) can be tiled *or* scaled. See [Picture](./picture.md) property for details.


The [OnTop](./ontop.md) property is either 0 or 1. If it
is 0, the Form assumes its normal position within the stack of windows on the
screen and is only brought to the front when it receives the input focus. If [OnTop](./ontop.md) is set to 1, the Form is always brought to the front even when it doesn't have
the focus. If more than one Form has [OnTop](./ontop.md) set to 1, the stacking order of this set of Forms is defined by the order in
which they were created.


A Form can be created as a child of another Form. If so, it has the following
characteristics:

- A child Form always appears on top of its parent Form (although it is not
    constrained by it)
- When you minimize a parent Form, its child Forms disappear.
- Making the parent Form invisible or inactive has no effect on a Child
    Form.

Note that the [Posn](./posn.md) and [Size](./size.md) properties of a child Form are expressed in screen coordinates and are not given
relative to its parent.


