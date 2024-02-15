




<h1 class="heading"><span class="name">NewLine</span></h1>

| Applies To: | [CoolBand](./coolband.md) |
| --- | ---  |


**Description**


The NewLine property specifies whether or not a [CoolBand](./coolband.md) occupies the same row as an existing [CoolBand](./coolband.md), or is displayed on a new line within its [CoolBar](./coolbar.md) parent.


NewLine is a single number with the value 0 (same row) or 1 (new row); the default is 1.


The value of NewLine in the first [CoolBand](./coolband.md) in a [CoolBar](./coolbar.md) is always 1, even if you specify it to be 0.


When the user drags a [CoolBand](./coolband.md) to another row, the value of its NewLine property, and that of any other [CoolBand](./coolband.md) affected by the move, will change.


You may move a [CoolBand](./coolband.md) to the previous or next row by changing its NewLine property (using `⎕WS` )from 1 to 0, or from 0 to 1 respectively.



