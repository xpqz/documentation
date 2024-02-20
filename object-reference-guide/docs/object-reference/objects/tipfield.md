




<h1 class="heading"><span class="name">TipField</span></h1>

[Parents](../ParentLists/TipField.htm) [Children](../ChildLists/TipField.htm) [Properties](../PropLists/TipField.htm) [Methods](../MethodLists/TipField.htm) [Events](../EventLists/TipField.htm)


Purpose: To display pop-up help.


**Description**


The TipField is used to display pop-up help when the user moves the mouse pointer over an object.



Most of the GUI objects supported by Dyalog APL/W have a [Tip](../a-z/tip.md) and a [TipObj](../a-z/tipobj.md) property. [TipObj](../a-z/tipobj.md) specifies the name of, or ref to, a TipField object, and [Tip](../a-z/tip.md) specifies a "help" message. The TipField automatically pops-up to display the [Tip](../a-z/tip.md) when the user moves the mouse pointer over the object. It disappears when the user moves the mouse pointer away.


The TipField is a simple box with a 1-pixel black border in which the text specified by [Tip](../a-z/tip.md) is displayed. [FCol](../a-z/fcol.md), [BCol](../a-z/bcol.md) and [FontObj](../a-z/fontobj.md) can be used to customise the appearance of the text within the box. [FCol](../a-z/fcol.md) specifies the colour of the text; [BCol](../a-z/bcol.md) specifies the background colour with which the box is filled. The default is black on yellow.


If you wish to display [Tip](../a-z/tip.md)s for particular objects in different fonts and colours, you must create a separate TipField for each combination of colour and font you need.


