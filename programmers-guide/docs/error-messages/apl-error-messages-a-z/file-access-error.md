




<h1 class="heading"><span class="name">FILE ACCESS ERROR</span><span class="command">19</span></h1>

This report is given when the user attempts to execute a file system function for which the user is not authorised, or has supplied the wrong passnumber.  It also occurs if the file specified as the argument to `⎕FERASE` or `⎕FRENAME` is not exclusively tied.

#### Examples
```apl
      'SALES' ⎕FSTIE 1
 
      ⎕FRDAC 1
0 4121 0
0 4137 99
 
      X ⎕FREPLACE 1
FILE ACCESS ERROR
      X ⎕FREPLACE 1
      ^
 
      'SALES' ⎕FERASE 1
FILE ACCESS ERROR
      'SALES' ⎕FERASE 1
      ^
```



