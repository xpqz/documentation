




<h1 class="heading"><span class="name">warning unmatched brackets</span></h1>

This report is given after adding or editing a function line in definition mode when it is found that there is not an opening bracket to match a closing bracket, or vice versa, in an expression.  This is a warning message only.  The function line will be accepted even though syntactically incorrect.

#### Example
```apl
[3]   A[;B[;2]←0
warning unmatched brackets
[4]
```



