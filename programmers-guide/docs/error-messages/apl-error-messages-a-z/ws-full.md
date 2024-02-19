




<h1 class="heading"><span class="name">WS FULL</span><span class="command">1</span></h1>

This report is given when there is insufficient workspace in which to perform an operation.  Workspace available is identified by the system constant `⎕WA`.


The maximum workspace size allowed is defined by the environment variable `MAXWS`. See [maxws parameter](../../UserGuide/Installation and Configuration/Configuration Parameters.htm#maxws) for details.

#### Example
```apl

      ⎕WA⍴1.2
WS FULL
      ⎕WA⍴1.2
      ^
```



