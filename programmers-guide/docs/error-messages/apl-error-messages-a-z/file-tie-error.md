




<h1 class="heading"><span class="name">FILE TIE ERROR</span><span class="command">18</span></h1>

This report is given when the argument to a file system function contains a file tie number used as if it were tied when it is not or as if it were available when it is already tied.  It also occurs if the argument to `⎕FHOLD` contains the names of non-existent external variables. It does not indicate that there is a problem with the underlying operating system's locking mechanism.

#### Examples
```apl
      ⎕FNAMES,⎕FNUMS
SALES  1
COSTS  2
PROFIT 3
 
      X ⎕FAPPEND 4
FILE TIE ERROR
      X ⎕FAPPEND 4
      ^
      'NEWSALES' ⎕FCREATE 2
FILE TIE ERROR
      'NEWSALES' ⎕FCREATE 2
      ^
 
      'EXTVFILE' ⎕XT'BIGMAT'
      ⎕FHOLD 'BIGMAT'
FILE TIE ERROR
      ⎕FHOLD 'BIGMAT'
      ^
      ⎕FHOLD⊂'BIGMAT'
```



