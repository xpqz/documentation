




<h1 class="heading"><span class="name">TabObj</span></h1>

Applies To: [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [TabBtn](../a-z/tabbtn.md) [TabButton](../a-z/tabbutton.md) [TabControl](../a-z/tabcontrol.md)


**Description**


TabObj is a ref or a character vector.


TabObj associates a [SubForm](../a-z/subform.md) with a [TabBtn](../a-z/tabbtn.md) or a [TabButton](../a-z/tabbutton.md) object. Selecting the associated [TabBtn](../a-z/tabbtn.md) or [TabButton](../a-z/tabbutton.md) causes the [SubForm](../a-z/subform.md) to be given the input focus.


For a [SubForm](../a-z/subform.md), it specifies the name of, or ref to, a [TabBtn](../a-z/tabbtn.md) or [TabButton](../a-z/tabbutton.md) object that is to be associated with the [SubForm](../a-z/subform.md). When referenced or queried using `⎕WG`, TabObj returns a name if it was specified by a name, or a ref if it was specified by a ref.


For [TabBtn](../a-z/tabbtn.md) and [TabButton](../a-z/tabbutton.md) objects, TabObj is a read-only property that contains a ref to the associated [SubForm](../a-z/subform.md).


For a [TabBar](../a-z/tabbar.md) or [TabControl](../a-z/tabcontrol.md), TabObj is a read-only property that contains a ref to the currently selected [TabBtn](../a-z/tabbtn.md) or [TabButton](../a-z/tabbutton.md).



