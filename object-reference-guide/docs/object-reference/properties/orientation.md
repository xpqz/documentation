




<h1 class="heading"><span class="name">Orientation</span></h1>

| Applies To: | [Printer](../a-z/printer.md) |
| --- | ---  |


**Description**


The Orientation property specifies the orientation of the paper on a [Printer](../a-z/printer.md) object. It is a simple character vector which is either `'Portrait'` or `'Landscape'`. When you create a [Printer](../a-z/printer.md) object, the default value of the Orientation property is determined by the current setting for the corresponding printer device.


The effect of changing Orientation using `⎕WS` is to spool the current page (effectively the same as sending a NewPage event) and then to change the orientation of the paper. Note that the values of the first 2 elements of the DevCaps property change accordingly. You may also set Orientation when you create the [Printer](../a-z/printer.md) object with `⎕WC`. In neither case does the global setting for the printer device change.



