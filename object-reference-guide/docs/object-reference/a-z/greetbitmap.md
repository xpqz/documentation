




<h1 class="heading"><span class="name">GreetBitmap</span></h1>

Applies To: [Root](./root.md)


**Description**


This method is used to display or remove a bitmap, typically during
initialisation of a Dyalog runtime application.


The argument to GreetBitmap is `⍬` or a
2 element vector as follows:


| `[1]` | Display | 0 = off, 1 = on. |
| --- | --- | ---  |
| `[2]` | Bitmap file name | Character vector. |


If the argument is `⍬`, the bitmap is
removed.


The image may also be displayed initially by setting parameter: **greet_bitmap** on the command line, e.g.:
```apl
c:\myapp\dyalogrt greet_bitmap=mylogo myws
```


The image is displayed until either an untrapped error occurs, causing the
interpreter to (attempt to) display the session window, or the GreetBitmap
method is called.



