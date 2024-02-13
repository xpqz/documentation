




<h1 class="heading"><span class="name">warning unmatched parentheses</span></h1>

This report is given after adding or editing a function line in definition mode when it is found that there is not an opening parenthesis to match a closing parenthesis, or vice versa, in an expression.  This is a warning message only.  The function line will be accepted even though syntactically incorrect.

#### Example
```apl
[4]   X←(E>2)^E<10)⌿A
warning unmatched parentheses
[5]
```






