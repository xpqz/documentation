





<h1 class="heading"><span class="name">not saved this ws is name</span></h1>

This report is given in the following situations:

- When the system command `)SAVE` is used without a name, and the workspace is not named.  In this case the system reports `not``saved this ws is CLEAR WS`.
- When the system command `)SAVE` is used with a name, and that name is not the current name of the workspace, but is the name of an existing file.

In neither case is the workspace renamed.

#### Examples

```apl
      )CLEAR
      )SAVE
not saved this ws is CLEAR WS
 
      )WSID JOHND
      )SAVE
      )WSID ANDYS
      )SAVE JOHND
not saved this ws is ANDYS
```



