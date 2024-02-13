




<h1 class="heading"><span class="name">File Read Access</span><span class="command">R←⎕FRDAC Y</span></h1>
##### Access code 4096


`Y` must be a simple integer scalar or 1 or 2 element vector containing the file tie number followed by an optional passnumber.  If the passnumber is omitted it is assumed to be zero.  The result is the access matrix for the designated file.


For details see File Access Control on page 1
Programming Reference Guide: 

Component Files.

#### Examples
```apl

      ⎕FRDAC 1
28 2105 16385
 0 2073 16385
31   ¯1     0
```



