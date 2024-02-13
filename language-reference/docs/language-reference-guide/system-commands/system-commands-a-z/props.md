




<h1 class="heading"><span class="name">List Properties</span><span class="command">)PROPS</span></h1>

The `)PROPS` system command lists the Properties of the object associated with the current space.


For example:
```apl
      ⎕CS 'BB' ⎕WC 'BrowseBox' 
 
      )PROPS
BrowseFor       Caption ChildList       Data    Event
EventList       HasEdit KeepOnClose     MethodList
PropList        StartIn Target  Translate       Type
```


`)PROPS` produces no output when executed in a pure (non GUI) namespace, for example:
```apl
      ⎕CS 'X' ⎕NS ''
      )PROPS
```



