# The APL Command Line

The command line for Dyalog APL is described below; the command line for non-Windows versions of Dyalog APL is very similar and is also documented in **Dyalog for UNIX UI Guide: Starting APL**.

Usually the command line is specified in the Target: field of the APL shortcut. The full pathname to the Dyalog executable is usually surrounded by double quotes as it contains spaces.

### Command Line

dyalog [ options ] [ debug ] [ ws ] [param] [param] [param]...

where:

**[dyalog]**

| Is the location of the Dyalog executable. Usually this is the full pathname, surrounded by double quotes. |
| ---  |

**[options]**

| -x | Disables the execution of the `⎕LX` expression and the derived expression when code is loaded from a source code file or directory.  This applies only at start-up and does not apply to workspaces or source files that are loaded subsequently. See Latent Expression on page 1 and Load on page 1 |
| --- | ---  |
| -a | Start in USER mode. |
| -b | Suppress the banner in the Session.. |
| -s | Disable the Session. This option is ignored in Windows versions. |
| +s | Force the display of the Session when it would otherwise not be shown. |
| -q | Don't quit APL on error (used when piping input into APL). |
| +q | Quit APL on error. In earlier versions of Dyalog, quitting on error saved a workspace with the reserved name CONTINUE; this behaviour can be re-enabled using `2704⌶` . See Continue Autosave on page 1 . |
| -c | Signifies a command-line comment. All characters to the right are ignored. |
| -cef -cef_all | Instructs Dyalog to ignore the parameter that immediately follows or all the parameters that follow. These options are intended to isolate parameters intended for the built-in Chromium Embedded Framework (CEF). See HTMLRenderer on page 1 . |

**[debug]**

| -Dc | Check workspace integrity after every callback function. |
| --- | ---  |
| -Dw | Check workspace integrity on return to session input. |
| -DW | Check workspace integrity after every line of APL (application will run slowly as a result) |
| -DK | Log session keystrokes in (binary) file **./apllog** . |

**[ws]**

| The name of a Dyalog APL workspace to be loaded. Unless specified, on Windows the file extension .DWS is assumed. |
| ---  |

**[param]**

| A parameter name followed by an equals sign ( `=` ) and a value. The parameter name may be one of the standard APL parameters (see Configuration Parameters on page 1 ) or a name and value of your own choosing (see GetEnvironment Method GetEnvironment on page 1 ) . If the parameter is in a registry sub-folder (see Registry Sub-Folders on page 1 ), its name must be preceded by the name of the sub-folder, followed by a backslash ( `\` ) or underscore ( `_` ). |
| ---  |

Note that instead of  a loading a workspace specified by the **ws** option, APL can be instructed to load a program from a script file. For further information, see Load on page 1.

### Examples:

Start APL using the configuration file `myconfig.dcfg`:
```apl
`"c:\program files\…\dyalog.exe" ConfigFile="myconfig.dcfg"`
```

Load the workspace `myapp`, setting MaxWS parameter:
```apl
`"c:\program files\…\dyalog.exe" myapp maxws=2G`
```

Load the workspace `myapp`, set an application specific parameter, but do not execute the latent expression:
```apl
`"c:\program files\…\dyalog.exe" -x myapp myparam=8080`
```

Run the function defined in `myfn.aplf`:
```apl
`"c:\program files\…\dyalog.exe" load=myfn.aplf`
```

Start APL and output "Hello World":
```apl
`"c:\program files\…\dyalog.exe" lx=" ⎕←'Hello World' "`
```
