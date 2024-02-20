




<h1 class="heading"><span class="name">GetCommandLineArgs</span></h1>

Applies To: [Root](../a-z/root.md)


**Description**


The GetCommandLineArgs method returns the command and the arguments to the command that was used to start the current Dyalog APL session or application.


The GetCommandLineArgs method is niladic.


The result is a vector of character vectors. For example:
```apl
      GetCommandLineArgs
 C:\Dyalog10\dyalog.exe  -Dw  YY_WINDOW=-30
```
```apl
      DISPLAY 2 ⎕NQ '.' 'GetCommandLineArgs'
┌→───────────────────────────────────────────────┐
│ ┌→─────────────────────┐ ┌→──┐ ┌→────────────┐ │
│ │c:\dyalog10\dyalog.exe│ │-Dw│ │YY_WINDOW=-30│ │
│ └──────────────────────┘ └───┘ └─────────────┘ │
└∊───────────────────────────────────────────────┘
```



