# Structuring of Arrays

A class of primitive functions re-structures arrays in some way. Arrays may be input only in scalar or vector form. Structural functions may produce arrays with a higher rank. The Structural functions are reshape (`⍴`), ravel, laminate and catenate (`,`), reverse and rotate (`⌽`), transpose (`⍉`), mix and take (`↑`), split and drop (`↓`), enlist (`∊`), and enclose (`⊂`).

## Examples
```apl
      2 2⍴1 2 3 4
1 2
3 4
 
      2 2 4⍴'ABCDEFGHIJKLMNOP'
ABCD
EFGH
 
IJKL
MNOP
         ↓2 4⍴'COWSHENS'
 COWS  HENS
```
