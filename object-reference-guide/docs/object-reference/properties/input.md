




<h1 class="heading"><span class="name">Input</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


This property specifies objects to be associated with cells in a Grid.



These
objects may be of type [Button](../a-z/button.md), [ColorButton](../a-z/colorbutton.md),
[Combo](../a-z/combo.md), [Edit](../a-z/edit.md), [Label](../a-z/label.md),
[Spinner](../a-z/spinner.md) or [TrackBar](../a-z/trackbar.md).
In addition, the Input property may specify instances of [OCXClass](../a-z/ocxclass.md) objects (ActiveX controls) and [NetType](../a-z/nettype.md) objects (.NET classes).


The Input property is either a single ref or a simple character scalar or
vector, or a vector of character vectors or refs. If it specifies a single
object, this will be associated with *all* of the cells in the [Grid](../a-z/grid.md).
If it specifies a set of objects, these are mapped to individual cells through
the [CellTypes](../a-z/celltypes.md) property.


When a cell becomes the current cell, its value (defined by the appropriate
element of the [Values](../a-z/values.md) property) defines the
value of a *corresponding property*of the associated object The
property that corresponds to the value in the cell, depends upon the [Type](../a-z/type.md) of the associated object as shown in the following table:


| Associate Object Type | Corresponding Property |
| --- | ---  |
| [Label](../a-z/label.md) | [Text](../a-z/text.md) |
| [Edit](../a-z/edit.md) | [Value](../a-z/value.md) |
| [Combo](../a-z/combo.md) | [Text](../a-z/text.md) |
| [Button](../a-z/button.md) ( [Style](../a-z/style.md) Push) | [Caption](../a-z/caption.md) |
| [Button](../a-z/button.md) ( [Style](../a-z/style.md) Radio or Check) | [State](../a-z/state.md) |
| [ColorButton](../a-z/colorbutton.md) | [CurrentColor](../a-z/currentcolor.md) |
| [Spinner](../a-z/spinner.md) | [Value](../a-z/value.md) |
| [TrackBar](../a-z/trackbar.md) | [Thumb](../a-z/thumb.md) |
| [OCXClass](../a-z/ocxclass.md) | Specified by [InputProperties](../a-z/inputproperties.md) |
| [NetType](../a-z/nettype.md) | Specified by [InputProperties](../a-z/inputproperties.md) |


In effect, the user inputs a new value into the current cell by changing the
corresponding property of its associated object. An associated object may be a *fixed* object that is *external* to the [Grid](../a-z/grid.md) or a *floating* object that moves automatically from cell to cell. The latter is achieved by
creating the associated object as a *child* of the [Grid](../a-z/grid.md).


If the associated object is an [Edit](../a-z/edit.md) or [Combo](../a-z/combo.md),
the user may change the [Text](../a-z/text.md) property of the
object by typing, or, in the case of a [Combo](../a-z/combo.md),
by selecting an item from a list. The new value of the [Text](../a-z/text.md) property is then used to update the value in the cell (defined by the [Values](../a-z/values.md) property of the [Grid](../a-z/grid.md)) when the user moves on. If
the associated object is a radio button, the value in the cell (0 or 1) is
reflected by the [State](../a-z/state.md) property of the [Button](../a-z/button.md).
The user may click the [Button](../a-z/button.md) on and off,
changing its [State](../a-z/state.md) and thereby the
corresponding value in the cell.


If the associated object is a [ColorButton](../a-z/colorbutton.md),
the corresponding elements of the [Values](../a-z/values.md) property contain 3-element integer vectors which specify the RGB colour values.


If the associated object is an instance of an [OCXClass](../a-z/ocxclass.md) object (ActiveX control) or a [NetType](../a-z/nettype.md) object
(.NET class), the Grid uses the *default* property of the external object
if it has one. Alternatively, the [InputProperties](../a-z/inputproperties.md) property is used to specify which property (or properties) of the external
object are to be mapped to elements of [Values](../a-z/values.md).
If more than one property is specified, elements of [Values](../a-z/values.md) are vectors.


If there is no object associated with a cell, or if its associated object is
a [Label](../a-z/label.md) or a [Button](../a-z/button.md) with [Style](../a-z/style.md) Push, the cell is protected and
may not be changed by the user. When the current cell is thus protected, the
corresponding row and column titles are not indented as they are when the cell
may be edited.


If the associated object is a numeric [Edit](../a-z/edit.md) or
[Label](../a-z/label.md) ([FieldType](../a-z/fieldtype.md) Numeric, LongNumeric, Currency, Date, LongDate or Time) the contents of the cell
are formatted accordingly, even when it is not the current cell. Thus a cell
associated with a [Label](../a-z/label.md) with [FieldType](../a-z/fieldtype.md) Date, always displays as a date.


If the associated object is a [Combo](../a-z/combo.md) or [Button](../a-z/button.md),
the appearance of a non-current cell is defined by the corresponding element of
the [ShowInput](../a-z/showinput.md) property.



The following example illustrates the use of different types of object
specified by the Input and [ShowInput](../a-z/showinput.md) properties:


![input](../img/input.gif)



