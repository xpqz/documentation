




<h1 class="heading"><span class="name">File Set Access</span><span class="command">{R}←X ⎕FSTAC Y</span></h1>
##### Access code 8192


`Y` must be a simple integer scalar or 1 or 2 element vector containing the file tie number followed by an optional passnumber. If the passnumber is omitted it is assumed to be zero.


`X` must be a valid access matrix, i.e. a 3-column integer matrix with any number of rows.  The function sets access control for a set of specific users (1<sup>st</sup> column) and file operations (2<sup>nd</sup> column) with specified passnumbers ( 3<sup>rd</sup> column). Note that a 0 in the 1<sup>st</sup> column specifies **all** users, a `¯1` in the 2<sup>nd</sup> column specifies **all** file operations, and a `0` in the 3<sup>rd</sup> column specifies that **no** passnumber is required. For further details, see [File Access Control](../APL Component Files/Component Files.htm#File_Access_Control).


The shy result of `⎕FSTAC` is the tie number of the file.

#### Examples
```apl

      'SALES' ⎕FCREATE 1
      (3 3⍴28 2105 16385 0 2073 16385 31 ¯1 0) ⎕FSTAC 1
      ((⎕FRDAC 1)⍪21 2105 16385) ⎕FSTAC 1

       (1 3⍴0 ¯1 0)⎕FSTAC 2 ⍝ Let everyone do anything

```



