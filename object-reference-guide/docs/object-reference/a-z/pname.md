




<h1 class="heading"><span class="name">PName</span></h1>

Applies To: [Font](./font.md) [Printer](./printer.md)


**Description**


This property is a character vector that specifies the face name for a [Font](./font.md) object, or the printing device associated with a [Printer](./printer.md). It is case-independent.


For a [Printer](./printer.md), PName contains the description of the printer followed by a comma (,) and then the device to which it is attached.

#### Example:
```apl
      'PR1' ⎕WC 'Printer'
      'PR1' ⎕WG 'PName'
HP Universal Printing PS,hp4200
```



