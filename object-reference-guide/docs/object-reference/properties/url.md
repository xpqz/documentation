




<h1 class="heading"><span class="name">URL</span></h1>

| Applies To: | [HTMLRenderer](../a-z/htmlrenderer.md) |
| --- | ---  |


**Description**


The URL property is a character vector that  specifies the url of a resource to be requested by the [HTMLRenderer](../a-z/htmlrenderer.md). Its default value is an empty character vector.


Specifying URL is an alternative way to setting the [HTML](../a-z/html.md) property in order to display content in the [HTMLRenderer](../a-z/htmlrenderer.md).


When you set the URL property, the [HTMLRenderer](../a-z/htmlrenderer.md) will request the corresponding resource (from either the internet or the workspace via an [HTTPRequest](../a-z/httprequest.md) event) and the display will change according to the response. The [HTML](../a-z/html.md) property is ignored and remains unchanged.


When you set the [HTML](../a-z/html.md) property, the content of the [HTMLRenderer](../a-z/htmlrenderer.md) will change accordingly. The current value of the URL property is ignored and remains unchanged.


If you set BOTH URL and [HTML](../a-z/html.md) in the same statement, the value of URL takes precedence and the assignment to [HTML](../a-z/html.md) is ignored (it remains unchanged).



