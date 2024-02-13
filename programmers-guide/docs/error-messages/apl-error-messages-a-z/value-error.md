




<h1 class="heading"><span class="name">VALUE ERROR</span><span class="command">6</span></h1>

This report is given when either:

- There is no active definition for a name encountered in an expression.
- A function does not return a result in a context where a result is required.
#### Examples
```apl
     X
VALUE ERROR
     X
     ^
 
     ∇ HELLO
[1]    'HI THERE'
[2]  ∇
 
     2+HELLO
HI THERE
VALUE ERROR
     2+HELLO
      ^
```



