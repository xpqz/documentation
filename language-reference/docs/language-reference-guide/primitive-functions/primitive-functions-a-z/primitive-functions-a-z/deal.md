




<h1 class="heading"><span class="name">Deal</span><span class="command">R←X?Y</span></h1>

`Y` must be a simple scalar or 1-element vector containing a non-negative integer. `X` must be a simple scalar or 1-element vector containing a non-negative integer and `X≤Y`.


`R` is an integer  vector obtained by making `X` random selections from `⍳Y` without repetition.

#### Examples
```apl

      13?52
7 40 24 28 12 3 36 49 20 44 2 35 1

      13?52
20 4 22 36 31 49 45 28 5 35 37 48 40
```


`⎕IO` and `⎕RL` are implicit arguments of Deal. A side effect of Deal is to change the value of `⎕RL`. See ["Random Link: " on page 1](../../../system-functions/system-functions-a-z/system-functions-a-z/rl.md).



