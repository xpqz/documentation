




<h1 class="heading"><span class="name">Nor</span><span class="command">R←X⍱Y</span></h1>

`Y` must be a Boolean array.  `X` must be a Boolean array.  `R` is Boolean.  The value of `R` is the truth value of the proposition "neither `X` nor `Y`", and is determined as follows:
```apl
             X   Y     R
      
             0   0     1
             0   1     0
             1   0     0
             1   1     0
```

#### Example
```apl
      0 0 1 1 ⍱ 0 1 0 1
1 0 0 0
```



