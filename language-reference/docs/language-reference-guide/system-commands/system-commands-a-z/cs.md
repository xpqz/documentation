




<h1 class="heading"><span class="name">Change Space</span><span class="command">)CS {nm}</span></h1>

`)CS` changes the current space to the **global** namespace `nm`.


If no `nm` is given, the system changes to the top level (Root) namespace. If `nm` is not the name of a global namespace, the system reports the error message `Namespace does not exist`.


`name` may be either a simple name or a compound name separated by '`.`', including one of the special names `'#'` (Root) or `'##'` (Parent).


#### Examples
```apl
      )CS
#
      )CS X
#.X
      )CS Y.Z
#.X.Y.Z
      )CS ##
#.X.Y
      )CS #.UTIL
#.UTIL

```


