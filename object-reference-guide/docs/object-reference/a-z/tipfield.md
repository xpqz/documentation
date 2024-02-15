




<h1 class="heading"><span class="name">TipField</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | To display pop-up help. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| Children | [Detach](./detach.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| Properties | [Detach](./detach.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| Methods | [Detach](./detach.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| Events | [Detach](./detach.md) [ChooseFont](./choosefont.md) | [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |
| [Detach](./detach.md) | [ChooseFont](./choosefont.md) |  |


Description


The TipField is used to display pop-up help when the user moves the mouse pointer over an object.



Most of the GUI objects supported by Dyalog APL/W have a [Tip](./tip.md) and a [TipObj](./tipobj.md) property. [TipObj](./tipobj.md) specifies the name of, or ref to, a TipField object, and [Tip](./tip.md) specifies a "help" message. The TipField automatically pops-up to display the [Tip](./tip.md) when the user moves the mouse pointer over the object. It disappears when the user moves the mouse pointer away.


The TipField is a simple box with a 1-pixel black border in which the text specified by [Tip](./tip.md) is displayed. [FCol](./fcol.md), [BCol](./bcol.md) and [FontObj](./fontobj.md) can be used to customise the appearance of the text within the box. [FCol](./fcol.md) specifies the colour of the text; [BCol](./bcol.md) specifies the background colour with which the box is filled. The default is black on yellow.


If you wish to display [Tip](./tip.md)s for particular objects in different fonts and colours, you must create a separate TipField for each combination of colour and font you need.


