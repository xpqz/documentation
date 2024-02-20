




<h1 class="heading"><span class="name">Membership</span><span class="command">R←X∊Y</span></h1>

`Y` may be any array.  `X` may be any array.  `R` is Boolean. An element of `R` is 1 if the corresponding element of `X` can be found in `Y`.


An element of `X` is considered identical to an element in `Y` if `X≡Y` returns 1 for those elements.


`⎕CT` and `⎕DCT` are  implicit arguments of Membership.

#### Examples
```apl
      'THIS NOUN' ∊ 'THAT WORD'
1 1 0 0 1 0 1 0 0
 
      'CAT' 'DOG' 'MOUSE' ∊ 'CAT' 'FOX' 'DOG' 'LLAMA'
1 1 0
```



For performance information, see  
Programming Reference Guide: 

Search Functions and Hash Tables[Programmer's Guide: "Search Functions and Hash Tables"](../../Language/Defined Functions and Operators/Search Functions and Hash.htm#SearchFunctionsAndHashTables).


