




<h1 class="heading"><span class="name">Event Number</span><span class="command">R←⎕EN</span></h1>

This simple integer scalar reports the identification number for the most recent event which occurred, caused by an APL action or by an interrupt or by the `⎕SIGNAL` system function.  Its value in a clear workspace is `0`.

#### Example
```apl

      ÷0
DOMAIN ERROR: Divide by zero
      ÷0
     ∧
      ⎕EN
11
```


See ["APL Error Messages"](../../Language/Errors/APL Errors.htm#APLErrors)APL Error Messages



Note: `⎕SIGNAL` can be used to reset the value of this system constant.


