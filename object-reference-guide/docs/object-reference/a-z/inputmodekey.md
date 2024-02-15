




<h1 class="heading"><span class="name">InputModeKey</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


This property defines the keystroke used to switch from Scroll mode to InCell mode in a [Grid](./grid.md). It applies only where the [Grid](./grid.md) has a *floating*[Edit](./edit.md) control. See the description of the [InputMode](inputmode.md) property for further details.


The InputModeKey property is specified (in the same way as the [Accelerator](accelerator.md) property) as a 2-element vector of integer values containing the key number and shift state respectively. Its default is (113 0) which is "F2".


As an example, if you wanted to use Ctrl+Shift+a to switch modes, you would set InputModeKey to (65 3). 65 is the keynumber for "a" and 3 means Shift (1) + Ctrl (2).



