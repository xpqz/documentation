



<h1 class="heading"><span class="name">Undo</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


This method is used to undo the previous change in a [Grid](./grid.md) object.


The [Grid](./grid.md) object maintains a buffer of the most recent 8 changes made by the user since the [Values](./values.md) property was last set by [`⎕WC`](../../Language/System%20Functions/wc.htm) or [`⎕WS`](../../Language/System%20Functions/ws.htm).


Your application can restore these changes one by one by calling the Undo method on the [Grid](./grid.md). The Undo method restores the most recent change made by the user and removes that change from the undo stack.


It is therefore not possible to "undo an undo".


The argument to Undo is `⍬`, or a single item as follows :


| `[1]` | Number of changes | integer |
| --- | --- | ---  |


If called with an argument of `⍬`, the default value for the *Number of changes* is 1. This restores the most recent change.


