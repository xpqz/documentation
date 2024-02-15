




<h1 class="heading"><span class="name">Wrap</span></h1>
| Applies To: | [ListView](../a-z/listview.md) | [ProgressBar](../a-z/progressbar.md) | [Spinner](../a-z/spinner.md) | [UpDown](../a-z/updown.md) |
| --- | --- | --- | --- | ---  |

| Applies To: | [ListView](../a-z/listview.md) [ProgressBar](../a-z/progressbar.md) [Spinner](../a-z/spinner.md) [UpDown](../a-z/updown.md) | [ListView](../a-z/listview.md) | [ProgressBar](../a-z/progressbar.md) | [Spinner](../a-z/spinner.md) | [UpDown](../a-z/updown.md) |  |  |
| --- | --- | ---  |
| [ListView](../a-z/listview.md) | [ProgressBar](../a-z/progressbar.md) | [Spinner](../a-z/spinner.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


The Wrap property is Boolean and has a default value of 1.


For a [ListView](../a-z/listview.md) it specifies whether or not long labels (specified by the Items property) may be wrapped or not.


For a [ProgressBar](../a-z/progressbar.md) object it determines whether or not the object starts over again when it reaches its upper limit. In particular, if Wrap is 1, the value obtained when you set the Thumb property is given by the expression: `LIMITS[1]+THUMB|LIMITS[2]`where `THUMB` is the value to which you set the Thumb property and `LIMITS` is the value of the Limits property.


For a [Spinner](../a-z/spinner.md), Wrap determines what happens when the value in the [Spinner](../a-z/spinner.md) reaches its upper or lower limit. If Wrap is 1 the [Spinner](../a-z/spinner.md) will wrap around to its opposite limit. Otherwise it will stick.



