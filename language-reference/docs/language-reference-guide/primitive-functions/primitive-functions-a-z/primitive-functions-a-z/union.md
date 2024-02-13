




<h1 class="heading"><span class="name">Union</span><span class="command">R←X∪Y</span></h1>

`Y` must be a vector.  `X` must be a vector.  If either argument is a scalar, it is treated as a one-element vector.  `R` is a vector of the elements of `X` catenated with the elements of `Y` which are not found in `X`.


Items in `X` and `Y` are considered the same if `X≡Y` returns 1 for those items.


`⎕CT` and `⎕DCT` are  implicit arguments of Union.

#### Examples
```apl
      'WASH' ∪ 'SHOUT'
WASHOUT
 
      'ONE' 'TWO' ∪ 'TWO' 'THREE'
 ONE  TWO  THREE
```



For performance information, see  
Programming Reference Guide: 

Search Functions and Hash TablesProgrammer's Guide: "Search Functions and Hash Tables".


