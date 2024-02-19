# Structuring of Arrays

A class of primitive functions re-structures arrays in some way. Arrays may be input only in scalar or vector form. Structural functions may produce arrays with a higher rank. The Structural functions are [reshape](../../Primitive Functions/Reshape.htm#Reshape) (`⍴`), [ravel](../../Primitive Functions/Ravel.htm#Ravel), [laminate and catenate](../../Primitive Functions/Catenate Laminate.htm#Catenate/Laminate) (`,`), [reverse](../../Primitive Functions/Reverse.htm#Reverse) and [rotate](../../Primitive Functions/Rotate.htm#Rotate) (`⌽`), [transpose](../../Primitive Functions/Transpose Monadic.htm#Transpose(Monadic)) (`⍉`), [mix](../../Primitive Functions/Mix.htm#Mix) and [take](../../Primitive Functions/Take.htm#Take) (`↑`), [split](../../Primitive Functions/Split.htm#Split) and [drop](../../Primitive Functions/Drop.htm#Drop) (`↓`), [enlist](../../Primitive Functions/Enlist.htm#Enlist) (`∊`), and [enclose](../../Primitive Functions/Enclose.htm#Enclose) (`⊂`).

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
