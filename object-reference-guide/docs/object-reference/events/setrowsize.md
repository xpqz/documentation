




<h1 class="heading"><span class="name">SetRowSize</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


If enabled, this event is reported when the user changes the height of a row or changes the height of the column titles. This may be done by dragging a border with the mouse or by double-clicking over a border. In the former case, the default action is to adjust the height of the appropriate row or the height of the column title area to the size selected by the user. In the latter case, the default action is to adjust the height to the maximum required to display all the data.



In either case, you can disable the default action by setting the event action code to `¯1` or you can selectively prevent a particular resize operation from taking place by returning 0 from a callback function.



The event message reported as the result of [`⎕DQ`](../../Language/System%20Functions/dq.htm), or supplied as the right argument to your callback function, is a 5-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'SelRowSize'` or 175 |
| `[3]` | Row number | Integer. This is sensitive to the index origin, `⎕IO` , but is `¯1` if the user has resized the column titles. |
| `[4]` | Height | Integer containing the value of the (new) row height. This is `¯3` if the user has double-clicked to request automatic height adjustment. |
| `[5]` | Undo flag | 0 or 1 |




You can resize a row or resize the column titles under program control by calling SetRowSize as a method. If you specify `¯1` as the *Height* parameter, the row will be resized to its default height .. If you specify a value of `¯2` the row will be resized to fit the data. The following expression will set the heights of first `NROWS` rows of a Grid called `F.G` to fit the data and the row titles.
```apl
      {F.G.SetRowSize ⍵ ¯3}¨⍳NROWS
```



The Undo flag is always 1 if the event was generated by the user.

