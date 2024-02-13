




<h1 class="heading"><span class="name">Remove Data Binding</span><span class="command">R←2014⌶Y</span></h1>

This function disassociates a data-bound variable from its data binding source.


`Y` is any array.


If `Y` or an element of `Y` is a character vector that contains the name of a data-bound variable, that variable is dissociated from its data binding source.


The result `R` is always 1.

#### Example
```apl

      2014⌶'txtSource'
1    
```



.NET Framework only


