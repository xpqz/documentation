




<h1 class="heading"><span class="name">MultiSelect</span></h1>
| Applies To: | [TabControl](../a-z/tabcontrol.md) |
| --- | ---  |

| Applies To: | [TabControl](../a-z/tabcontrol.md) | [TabControl](../a-z/tabcontrol.md) |  |  |
| --- | --- | ---  |
| [TabControl](../a-z/tabcontrol.md) |  |  |


Description


The [TabControl](../a-z/tabcontrol.md) property specifies whether or not the user can select more than one button in a [TabControl](../a-z/tabcontrol.md) at the same time, by holding down the Ctrl key when clicking.


MultiSelect is a single number with the value 0 (only 1 button may be selected) or 1 (more than one button may be selected); the default is 0.


MultiSelect apples only if the [Style](../a-z/style.md) of the [TabControl](../a-z/tabcontrol.md) is `'Buttons'` or `'FlatButtons'`, and is ignored if [Style](../a-z/style.md) is `'Tabs'`.


Note that the [State](../a-z/state.md) property of the associated [TabButton](../a-z/tabbutton.md) object reports whether or not the button is selected.



