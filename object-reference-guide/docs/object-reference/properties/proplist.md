




<h1 class="heading"><span class="name">PropList</span></h1>

**Applies To**


**Description**


This is a "read-only" property that supplies a list of all other properties which are applicable to the object in question. The list is returned as a vector of character vectors in the order in which the corresponding properties are expected by [`⎕WC`](../../Language/System Functions/wc.htm) and [`⎕WS`](../../Language/System Functions/ws.htm).

#### Example:
```apl
      'F'    ⎕WC 'Form'
      'F.MB' ⎕WC 'MenuBar'
      'F.MB' ⎕WG 'PropList'
 Type  Visible  FontObj  Data  EdgeStyle  MDIMenu  PropList
```



