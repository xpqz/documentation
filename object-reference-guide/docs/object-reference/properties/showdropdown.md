




<h1 class="heading"><span class="name">ShowDropDown</span></h1>

Applies To: [ColorButton](../a-z/colorbutton.md) [ToolControl](../a-z/toolcontrol.md)


**Description**


The ShowDropDown property specifies whether or not a drop-down menu symbol is drawn in a [ColorButton](../a-z/colorbutton.md) or alongside [ToolButton](../a-z/toolbutton.md) objects which have [Style ](../a-z/style.md)`'DropDown'`.



ShowDropDown is a single number with the value 0 (drop-downs captions are not shown) or 1 (drop-downs **are** shown); the default is 1.


ShowDropDown also affects the behaviour of [ToolButton](../a-z/toolbutton.md) objects which have Style `'DropDown'`.


If the ShowDropDown property of the parent [ToolControl](../a-z/toolcontrol.md) is 0, clicking the [ToolButton](../a-z/toolbutton.md) causes the popup menu to appear. In this case, the [ToolButton](../a-z/toolbutton.md) itself does not itself generate a Select event; you must rely on the user selecting a MenuItem to specify a particular action.


If the ShowDropDown  property of the parent [ToolControl](../a-z/toolcontrol.md) is 1, clicking the dropdown button causes the popup menu to appear; clicking the [ToolButton](../a-z/toolbutton.md) itself generates a Select event, but does not display the popup menu.



The following picture illustrates a [ToolControl](../a-z/toolcontrol.md) with ShowDropDown set to 1:


![tool9](../img/tool9.gif)



