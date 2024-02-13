




<h1 class="heading"><span class="name">Excluding</span><span class="command">R←X~Y</span></h1>

`X` must be a scalar or vector.  `R` is a vector of the elements of `X` excluding those elements which occur in `Y` taken in the order in which they occur in `X`.


Elements of `X` and `Y` are considered the same if `X≡Y` returns 1 for those elements.


`⎕CT` and `⎕DCT` are  implicit arguments of Excluding. Excluding is also known as Without.

#### Examples
```apl
      'HELLO'~'GOODBYE'
HLL
      'MONDAY' 'TUESDAY' 'WEDNESDAY'~'TUESDAY' 'FRIDAY'
 MONDAY  WEDNESDAY
 
      5 10 15~⍳10
15
```



For performance information, see  
Programming Reference Guide: 

Search Functions and Hash TablesProgrammer's Guide: "Search Functions and Hash Tables".


