




<h1 class="heading"><span class="name">Unique</span><span class="command">R←∪Y</span></h1>

`Y` may be any array. `R` is a vector of the unique major cells of `Y` (the unique items of a vector, the unique rows of a matrix and so forth), in the order in which they first appear in `Y`.  For further information, see [Major Cells on page 1](../Introduction/Variables/Cells and Subarrays.htm#Major_Cells).


`⎕CT` and `⎕DCT` are  implicit arguments of Unique.


#### Examples
```apl

      ∪ 22 10 22 22 21 10 5 10
22 10 21 5

      ∪ v←'CAT' 'DOG' 'CAT' 'DUCK' 'DOG' 'DUCK'
┌───┬───┬────┐
│CAT│DOG│DUCK│
└───┴───┴────┘
      ⊢mat←↑v                                   
CAT 
DOG 
CAT 
DUCK
DOG 
DUCK
      ∪mat                                       
CAT 
DOG 
DUCK

```
```apl
      a←3 4 5⍴⍳20
      a
 1  2  3  4  5
 6  7  8  9 10
11 12 13 14 15
16 17 18 19 20
              
 1  2  3  4  5
 6  7  8  9 10
11 12 13 14 15
16 17 18 19 20
              
 1  2  3  4  5
 6  7  8  9 10
11 12 13 14 15
16 17 18 19 20
      ∪a
 1  2  3  4  5
 6  7  8  9 10
11 12 13 14 15
16 17 18 19 20

```


