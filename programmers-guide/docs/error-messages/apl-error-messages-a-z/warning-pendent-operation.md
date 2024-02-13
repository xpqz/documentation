




<h1 class="heading"><span class="name">warning pendent operation</span></h1>

This report is given on opening and closing definition mode when attempting to edit a pendant function or operator.

#### Example
```apl
[0]   ∇FOO
[1]    GOO
[2]   ∇
 
[0]   ∇GOO
[1]    ∘
[2]   ∇
 
      FOO
SYNTAX ERROR
GOO[1] ∘
       ^
 
      ∇FOO
warning pendent operation
[0]   ∇FOO
[1]    GOO
[2]   ∇
warning pendent operation
```



