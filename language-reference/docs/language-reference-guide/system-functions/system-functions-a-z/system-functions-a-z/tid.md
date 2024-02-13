




<h1 class="heading"><span class="name">Current Thread Identity</span><span class="command">R←⎕TID</span></h1>

`R` is a simple integer scalar whose value is the number of the current thread.

#### Examples
```apl
      ⎕TID     ⍝ Base thread number
0
 
      ⍎&'⎕TID' ⍝ Thread number of async ⍎.
1
```



