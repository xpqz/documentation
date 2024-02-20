




<h1 class="heading"><span class="name">Execute (UNIX) Command</span><span class="command">{R}←⎕SH Y</span></h1>

`⎕SH` executes a UNIX shell or a Windows Command Processor.  `⎕SH` is a synonym of `⎕CMD`.  Either function may be used in either environment (UNIX or Windows) with exactly the same effect.  `⎕SH` is probably more natural for the UNIX user.  This section describes the behaviour of `⎕SH` and `⎕CMD` under UNIX.  See ["Execute Windows Command: "](../../../system-functions-a-z/system-functions-a-z/execute-windows-command.md) for a discussion of the behaviour of these system functions under Windows.



`Y` must be a simple character scalar or vector representing a UNIX shell command.  `R` is a nested vector of character vectors.


`Y` may be any acceptable UNIX command. If the command does not produce any output, `R` is `0⍴⊂''` but the result is suppressed if not explicitly used or assigned.  If the command has a non-zero exit code, then APL will signal a `DOMAIN ERROR`.  If the command returns a result and has a zero exit code, then each element of `R` will be a line from the standard output (stdout) of the command.  Output from standard error (stderr) is not captured unless redirected to stdout.

#### Examples
```apl
      ⎕SH'ls'
FILES WS temp
 
      ⎕SH 'rm WS/TEST'
 
      ⎕SH 'grep bin /etc/passwd ; exit 0'
bin:!:2:2::/bin:
 
      ⎕SH 'apl MYWS <inputfile >out1 2>out2 &'
```


The system commands [`)SH`](../../../../system-commands/system-commands-a-z/sh.md) and [`)CMD`](../../../../system-commands/system-commands-a-z/cmd.md) provide similar facilities. For further information, see [Execute (UNIX) Command: ](../../../../system-commands/system-commands-a-z/sh.md) and [Example](../../../../system-commands/system-commands-a-z/cmd.md).

#### Note:


This function is disabled and instead generates a `DOMAIN ERROR` if the RIDE_SPAWNED parameter is non-zero. This is designed to prevent it being invoked from a RIDE session which does not support this type of user interface. For further details, see the **RIDE User Guide**.


Under macOS and Linux, if the configuration parameter ENABLE_CEF is 1 (which is the default), Auxiliary Processors may not be used (they hang on error).


