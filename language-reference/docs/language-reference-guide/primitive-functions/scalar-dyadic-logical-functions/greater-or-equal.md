




<h1 class="heading"><span class="name">Greater Or Equal</span><span class="command">R←X≥Y</span></h1>

`Y` must be numeric.  `X` must be numeric.  `R` is Boolean.  `R` is 1 if `X` is greater than `Y` or `X=Y`.  Otherwise `R` is 0.


`⎕CT` and `⎕DCT` are  implicit arguments of Greater Or Equal.

#### Examples
```apl
      1 2 3 4 5 ≥ 3
0 0 1 1 1
 
      ⎕CT←1E¯10
 
      1≥1
1
 
      1≥1.00000000001
1
 
      1≥1.00000001
0
```



