



<h1 class="heading"><span class="name">GetCommandLine</span></h1>
| Applies To: | [Root](../a-z/root.md) |
| --- | ---  |

| Applies To: | [Root](../a-z/root.md) | [Root](../a-z/root.md) |  |  |
| --- | --- | ---  |
| [Root](../a-z/root.md) |  |  |


Description


The GetCommandLine method returns the command line that was used to start the current Dyalog APL session or application.


The GetCommandLine method is niladic.


The result is a character vector.

#### Examples
```apl
      GetCommandLine
"C:\Program Files\Dyalog\Dyalog APL-64 13.2 Unicode\dyalog.exe"
```
```apl
      ⎕←2 ⎕NQ '.' 'GetCommandLine'
"C:\Program Files\Dyalog\Dyalog APL-64 13.2 Unicode\dyalog.exe"
```

#### Note


GetCommandLine only works on Windows, and its use is deprecated in favour of [GetCommandLineArgs](../a-z/getcommandlineargs.md), which works on all platforms.


