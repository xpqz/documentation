




<h1 class="heading"><span class="name">File Size</span><span class="command">R←⎕FSIZE Y</span></h1>

`Y` must be a simple integer scalar or 1 or 2 element vector containing the file tie number followed by an optional passnumber.  If the passnumber is omitted it is assumed to be zero.  The result is a 4 element numeric vector containing the following:

| Element | Description |
| --- | ---  |
| 1 | the number of first component |
| 2 | 1 + the number of the last component, (i.e. the result of the next `⎕FAPPEND` ) |
| 3 | the current size of the file in bytes |
| 4 | the file size limit in bytes |

#### Example
```apl
      ⎕FSIZE 1
1 21 65271 4294967295
```



