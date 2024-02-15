




<h1 class="heading"><span class="name">MultiSelect</span></h1>
| Applies To: | [TabControl](./tabcontrol.md) |
| --- | ---  |

| Applies To: | [TabControl](./tabcontrol.md) | [TabControl](./tabcontrol.md) |  |  |
| --- | --- | ---  |
| [TabControl](./tabcontrol.md) |  |  |


Description


The [TabControl](./tabcontrol.md) property specifies whether or not the user can select more than one button in a [TabControl](./tabcontrol.md) at the same time, by holding down the Ctrl key when clicking.


MultiSelect is a single number with the value 0 (only 1 button may be selected) or 1 (more than one button may be selected); the default is 0.


MultiSelect apples only if the [Style](style.md) of the [TabControl](./tabcontrol.md) is `'Buttons'` or `'FlatButtons'`, and is ignored if [Style](style.md) is `'Tabs'`.


Note that the State property of the associated [TabButton](./tabbutton.md) object reports whether or not the button is selected.



