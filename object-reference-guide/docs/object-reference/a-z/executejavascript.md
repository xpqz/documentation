




<h1 class="heading"><span class="name">ExecuteJavaScript</span></h1>
| Applies To: | [HTMLRenderer](./htmlrenderer.md) |
| --- | ---  |

| Applies To: | [HTMLRenderer](./htmlrenderer.md) | [HTMLRenderer](./htmlrenderer.md) |  |  |
| --- | --- | ---  |
| [HTMLRenderer](./htmlrenderer.md) |  |  |


Description


This method is used to execute JavaScript in an [HTMLRenderer](./htmlrenderer.md) object.


The argument to ExecuteJavaScript is a single item as follows:

| `[1]` | Code | character vector containing JavaScript code |
| --- | --- | ---  |


The shy result of ExecuteJavaScript is currently 1; this may change.

#### Example
```apl
      hr.ExecuteJavaScript 'alert("Hello")'
```



