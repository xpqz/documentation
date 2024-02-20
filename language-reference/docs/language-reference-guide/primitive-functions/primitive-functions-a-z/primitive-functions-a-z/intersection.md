




<h1 class="heading"><span class="name">Intersection</span><span class="command">R←X∩Y</span></h1>

`Y` must be  a scalar or vector.  `X` must be a scalar or vector.  A scalar `X` or `Y` is treated as a one-element vector.  `R` is a vector composed of items occurring in both `X` and `Y` in the order of occurrence in `X`.  If an item is repeated in `X` and also occurs in `Y`, the item is also repeated in `R`.


Items in `X` and `Y` are considered the same if `X≡Y` returns 1 for those items.


`⎕CT` and `⎕DCT` are  implicit arguments of Intersection.

#### Examples
```apl
      'ABRA'∩'CAR'
ARA
 
      1 'PLUS' 2 ∩ ⍳5
1 2
```



For performance information, see  
Programming Reference Guide: 

Search Functions and Hash Tables[Programmer's Guide: "Search Functions and Hash Tables"](../../Language/Defined Functions and Operators/Search Functions and Hash.htm#SearchFunctionsAndHashTables).


