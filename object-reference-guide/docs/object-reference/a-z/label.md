




<h1 class="heading"><span class="name">Label</span></h1>

| [Parents](../ParentLists/Label.htm) | [Children](../ChildLists/Label.htm) | [Properties](../PropLists/Label.htm) | [Methods](../MethodLists/Label.htm) | [Events](../EventLists/Label.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Displays static text. |
| --- | ---  |


**Description**


This object displays a text label, a number, a date or a time value.



If [FieldType](./fieldtype.md) is empty, the Label displays the text defined by its [Caption](./caption.md) property. If the [Caption](./caption.md) property contains one or more linefeed characters (`⎕UCS 10`) the Label becomes a multi-line Label which is top-left justified and automatically wraps on white-space characters (such as space and tab) to fit in the width provided.


If [FieldType](./fieldtype.md) is `'Numeric'`, `'LongNumeric'`, `'Currency'`, `'Date'`, `'LongDate'`, or `'Time'` the Label converts and formats the number defined by its [Value](./value.md) property and displays this instead. See [FieldType](./fieldtype.md) property for details.


The [Border](./border.md) property determines whether or not the label has a border. A value of 0 means no border (the default). A value of 1 means that a 1-pixel border is drawn around the label.


By default, the value of the [EdgeStyle](./edgestyle.md) property for a Label is `'None'` and the value of [BCol](./bcol.md) is 0 which is normally white, or grey if the parent object has a 3-dimensional appearance. You can change its appearance by setting [EdgeStyle](./edgestyle.md) and/or [BCol](./bcol.md) to different values.


