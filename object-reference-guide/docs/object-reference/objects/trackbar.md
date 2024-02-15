




<h1 class="heading"><span class="name">TrackBar</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The TrackBar object is a slider control that allows the user to enter a value by positioning a pointer (thumb) on a scale. |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) [GetTextSize](../a-z/gettextsize.md) [Animate](../a-z/animate.md) [GetFocus](../a-z/getfocus.md) [ShowSIP](../a-z/showsip.md) [GetFocusObj](../a-z/getfocusobj.md) | [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) | [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) |
| [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| Children | [Detach](../a-z/detach.md) [GetTextSize](../a-z/gettextsize.md) [Animate](../a-z/animate.md) [GetFocus](../a-z/getfocus.md) [ShowSIP](../a-z/showsip.md) [GetFocusObj](../a-z/getfocusobj.md) | [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) | [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) |
| [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| Properties | [Detach](../a-z/detach.md) [GetTextSize](../a-z/gettextsize.md) [Animate](../a-z/animate.md) [GetFocus](../a-z/getfocus.md) [ShowSIP](../a-z/showsip.md) [GetFocusObj](../a-z/getfocusobj.md) | [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) | [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) |
| [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| Methods | [Detach](../a-z/detach.md) [GetTextSize](../a-z/gettextsize.md) [Animate](../a-z/animate.md) [GetFocus](../a-z/getfocus.md) [ShowSIP](../a-z/showsip.md) [GetFocusObj](../a-z/getfocusobj.md) | [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) | [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) |
| [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| Events | [Detach](../a-z/detach.md) [GetTextSize](../a-z/gettextsize.md) [Animate](../a-z/animate.md) [GetFocus](../a-z/getfocus.md) [ShowSIP](../a-z/showsip.md) [GetFocusObj](../a-z/getfocusobj.md) | [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) | [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |
| [Detach](../a-z/detach.md) | [GetTextSize](../a-z/gettextsize.md) | [Animate](../a-z/animate.md) |
| [GetFocus](../a-z/getfocus.md) | [ShowSIP](../a-z/showsip.md) | [GetFocusObj](../a-z/getfocusobj.md) |


Description


The TrackBar object consists of a window which contains a slider bar, a thumb, and a set of tick marks. The slider in a TrackBar moves in increments that you specify when you create it. For example, if you specify that the TrackBar should have a range of five, the slider can only occupy six positions: a position at the left side of the TrackBar and one position for each increment in the range. Typically, each of these positions is identified by a tick mark. TrackBars can have either a vertical or horizontal orientation. They can have tick marks on either side, both sides, or neither. A selection of different TrackBars is illustrated below.



![track1](../img/track1.gif)


The position and size of the container window are defined by the [Posn](../a-z/posn.md) and [Size](../a-z/size.md) properties. Its appearance is defined by the [EdgeStyle](../a-z/edgestyle.md), [Border](../a-z/border.md) and [BCol](../a-z/bcol.md) properties. The defaults are `('EdgeStyle' 'None')`, `('Border' 0)` and `('BCol' 0)`. The default background colour `('BCol' 0)` obtains either the standard Window Background colour, or grey to match the colour of the parent object if it has a 3-dimensional appearance.


The orientation of a TrackBar is determined by the [HScroll](../a-z/hscroll.md) and [VScroll](../a-z/vscroll.md) properties. A horizontal TrackBar is obtained by setting [HScroll](../a-z/hscroll.md) to `¯1` and [VScroll](../a-z/vscroll.md) to 0. This is the default. A vertical TrackBar is obtained by setting [VScroll](../a-z/vscroll.md) to `¯1` and [HScroll](../a-z/hscroll.md) to 0.


[VScroll](../a-z/vscroll.md) and [HScroll](../a-z/hscroll.md) may only be set when the object is created and may not subsequently be changed.


The [ShowThumb](../a-z/showthumb.md) property determines whether or not the thumb is visible. Its default value is 1. You may toggle this property dynamically using `⎕WS`.


The TrackBar optionally displays tick marks at the two ends of the slider bar and spaced out along it. This behaviour is determined by the [HasTicks](../a-z/hasticks.md) property which may be 1 (the default) or 0 and may be set *only* when the object is created by `⎕WC`.


If [HasTicks](../a-z/hasticks.md) is 1, the position and frequency of the tick marks is determined by the [TickAlign](../a-z/tickalign.md) and [TickSpacing](../a-z/tickspacing.md) properties. Note that [TickAlign](../a-z/tickalign.md) may only be set when the TrackBar is created with `⎕WC` and may not be altered using `⎕WS`.


The slider and tick marks in a horizontal TrackBar are drawn along the top of the enclosing window. The slider and tick marks in a vertical TrackBar are drawn along the left edge of the window. The position and size of the slider and the thumb may be obtained from the [TrackRect](../a-z/trackrect.md) and [ThumbRect](../a-z/thumbrect.md) properties which report these values in pixels. These are *read-only* properties and cannot not be set with `⎕WC` or `⎕WS`.


The value of the TrackBar is determined by its [Thumb](../a-z/thumb.md) property which is an *integer* that may be set with `⎕WS` or retrieved with `⎕WG`. The [Limits](../a-z/limits.md) property specifies the minimum and maximum values of Thumb corresponding to its position at the two ends of the slider bar. The [Step](../a-z/step.md) property is a 2-element integer vector defining the small and large increments by which the Thumb moves. A small step is obtained by pressing a cursor movement key; a large step is achieved by clicking the left mouse button either side of the thumb or by pressing Page Up and Page Down. The user may also drag the thumb to a new position or move it directly to either end of the slider by pressing Home or End.


An alternative form of the TrackBar is obtained by setting the [Style](../a-z/style.md) property to `'Selection'`. This may only be done when the object is created using `⎕WC`. This style of TrackBar has a slider that is represented by a recessed thick white rectangle instead of a solid black line. Furthermore, you can select a range of values within the TrackBar by setting the [SelRange](../a-z/selrange.md) property. This causes the TrackBar to display a solid blue bar within the white slider and to show the corresponding tick marks as small triangles. Note that there is no way for the user to change [SelRange](../a-z/selrange.md) directly; you can only do this using `⎕WS`.


In addition to the normal mouse events, the TrackBar generates a [Scroll](../a-z/scroll.md) and [ThumbDrag](../a-z/thumbdrag.md) event. The [Scroll](../a-z/scroll.md) event is the same event that is generated by a Scroll object and is reported when the user repositions the thumb. If enabled, the [ThumbDrag](../a-z/thumbdrag.md) event is reported continuously as the user drags the thumb with the mouse and may be used to synchronise the display of a corresponding value in another object.


