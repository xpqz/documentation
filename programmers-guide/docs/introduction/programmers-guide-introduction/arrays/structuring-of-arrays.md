# Structuring of Arrays

A class of primitive functions re-structures arrays in some way. Arrays may be input only in scalar or vector form. Structural functions may produce arrays with a higher rank. The Structural functions are [reshape](../../Primitive%20Functions/Reshape.htm#Reshape) (`⍴`), [ravel](../../Primitive%20Functions/Ravel.htm#Ravel), [laminate and catenate](../../Primitive%20Functions/Catenate%20Laminate.htm#Catenate/Laminate) (`,`), [reverse](../../Primitive%20Functions/Reverse.htm#Reverse) and [rotate](../../Primitive%20Functions/Rotate.htm#Rotate) (`⌽`), [transpose](../../Primitive%20Functions/Transpose%20Monadic.htm#Transpose(Monadic)) (`⍉`), [mix](../../Primitive%20Functions/Mix.htm#Mix) and [take](../../Primitive%20Functions/Take.htm#Take) (`↑`), [split](../../Primitive%20Functions/Split.htm#Split) and [drop](../../Primitive%20Functions/Drop.htm#Drop) (`↓`), [enlist](../../Primitive%20Functions/Enlist.htm#Enlist) (`∊`), and [enclose](../../Primitive%20Functions/Enclose.htm#Enclose) (`⊂`).

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
