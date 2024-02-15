




<h1 class="heading"><span class="name">ScrollOpposite</span></h1>

| Applies To: | [TabControl](../a-z/tabcontrol.md) |
| --- | ---  |


**Description**


The ScrollOpposite property specifies that unneeded tabs scroll to the opposite side of a [TabControl](../a-z/tabcontrol.md), when a tab is selected.



ScrollOpposite is a single number with the value 0 (normal scrolling) or 1 (scrolling to the opposite side); the default is 0.



The picture below illustrates a [TabControl](../a-z/tabcontrol.md) with ScrollOpposite set to 1, after the user has clicked *Third Tab*.


![tab10](../img/tab10.gif)



Setting ScrollOpposite to 1 implies that [MultiLine](../a-z/multiline.md) is also 1. If you set ScrollOpposite to 1 in a `⎕WC` statement, the [MultiLine](../a-z/multiline.md) property will automatically be set to 1, even if you try to set [MultiLine](../a-z/multiline.md) to 0 in the same statement. If you subsequently change [MultiLine](../a-z/multiline.md) back to 0 using `⎕WS`, this will work, but the effect is not useful and it is not supported.


