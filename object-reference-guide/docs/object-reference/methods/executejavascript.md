




<h1 class="heading"><span class="name">ExecuteJavaScript</span></h1>

Applies To: [HTMLRenderer](../a-z/htmlrenderer.md)


**Description**


This method is used to execute JavaScript in an [HTMLRenderer](../a-z/htmlrenderer.md) object.


The argument to ExecuteJavaScript is a single item as follows:


`[1]` Code character vector containing JavaScript code


The shy result of ExecuteJavaScript is currently 1; this may change.

#### Example
```apl
      hr.ExecuteJavaScript 'alert("Hello")'
```



