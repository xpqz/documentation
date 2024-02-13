# Namelists

The right argument and the result of a function may be specified in the function header by a single name or by a *Namelist*. In this context, a Namelist is a blank-delimited list of names surrounded by a single set of parentheses.

Names specified in a Namelist are automatically local to the function; there is no need to localise them explicitly using semi-colons.

If the *right argument* of a function is declared as a Namelist, the function will only accept a right argument that is a vector whose length is the same as the number of names in the Namelist. Calling the function with any other argument will result in a `LENGTH ERROR` in the calling statement. Otherwise, the elements of the argument are assigned to the names in the Namelist in the specified order.

## Example:
```apl
     ∇ IDN←Date2IDN(Year Month Day)
[1]    'Year is ',⍕Year
[2]    'Month is ',⍕Month
[3]    'Day is ',⍕Day
[4] ...
     ∇
 
      Date2IDN 2004 4 30
Year is 2004
Month is 4
Day is 30
 
      Date2IDN 2004 4
LENGTH ERROR
      Date2IDN 2004 4
     ^
```

Note that if you specify a *single* name in the Namelist, the function may be called only with a 1-element vector right argument. If the *result* of a function is declared as a Namelist, the values of the names will automatically be stranded together in the specified order and returned as the result of the function when the function terminates.

## Example:
```apl
     ∇ (Year Month Day)←Birthday age
[1]    Year←1949+age
[2]    Month←4
[3]    Day←30
     ∇
      Birthday 50
1999 4 30
```
