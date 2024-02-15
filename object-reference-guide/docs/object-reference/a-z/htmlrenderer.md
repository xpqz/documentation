




<h1 class="heading"><span class="name">HTMLRenderer</span></h1>

| [Parents](../ParentLists/HTMLRenderer.htm) | [Children](../ChildLists/HTMLRenderer.htm) | [Properties](../PropLists/HTMLRenderer.htm) | [Methods](../MethodLists/HTMLRenderer.htm) | [Events](../EventLists/HTMLRenderer.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The HTMLRenderer Object is a cross-platform mechanism for producing Graphical User Interfaces (GUI), based on HyperText Markup Language (HTML). |
| --- | ---  |


**Description**


The HTMLRenderer object renders HTML in a window on the screen. It may appear as a top-level window, similar to a Form, or be displayed within another GUI object according to the value of the Boolean [AsChild](./aschild.md) property which must be specified when the HTMLRenderer is created. Several HTMLRenderer objects may co-exist in the Dyalog application.



The HTMLRenderer is implemented using the  [Chromium Embedded Framework (CEF).](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework) Note that if the  [ENABLE_CEF parameter](../../UserGuide/Installation%20and%20Configuration/Configuration%20Parameters.htm#ENABLE_CEF) is set to 0 (its default value is 1) the CEF is disabled and an attempt to create an HTMLRenderer object will fail with an error message.


The HTMLRenderer object can be considered as two components; a client implemented using CEF and an internal server which implements an interface from the APL workspace to the client.  The client may communicate with both the internal server and external servers on the web. Thus it can combine and display information from external and internal feeds.


Internal and external communications are distinguished primarily by the [InterceptedURLs](./interceptedurls.md) property which specifies which requests from the HTMLRenderer client component are to he handled by the internal server component and which are to be serviced by the internet. The default value of [InterceptedURLs](./interceptedurls.md) has been chosen so that in most cases it can be ignored.


The  HTMLRenderer object supports both the HTTP protocol and the WebSocket (WS) protocol.


Using the HTTP protocol, the client requests a resource, such as  a style-sheet, an image, or a complete web page, which the server then delivers. All communication is initiated by the client and involves the creating, use, and closing of a TCP/IP socket.


Using WS protocol,  the client asks the server for a permanent communications channel (this is done by *upgrading* the TCP/IP socket to a WebSocket) which may subsequently be used for  messages initiated by either the client or the server.


The internal server component of the HTMLRenderer is implemented by functions in the workspace.


HTTP protocol communications are handled by  callback functions on the [HTTPRequest](./httprequest.md) event.


WS protocol communications are handled:

- by  the [WebSocketUpgrade](./websocketupgrade.md) event, which reports the initial connection and the WebSocket ID,
- by a callback on the [WebSocketReceive](./websocketreceive.md) event
- and by calling the [WebSocketSend](./websocketsend.md) method.

The HTMLRenderer may be initialised by setting its [HTML](./html.md) property to a character vector representing a base HTML document. This will typically contain references to other documents,  such as JavaScript and CSS files which contain code that can influence the way the base HTML is rendered, image files in a variety of formats, and of course hyperlinks to other pages.


If the HTML contains references to other documents, the CEF will retrieve each one by making an HTTP request. Requests with URLs that match a triggering pattern in the [InterceptedURLs](./interceptedurls.md) property will generate an [HTTPRequest](./httprequest.md) event on the HTMLRenderer, which can be directed to a callback function.


Requests with URLs that do not match a pattern in [InterceptedURLs](./interceptedurls.md), or that match a pattern with a 0 in the second column, will be handled by the CEF.


Requests handled by the CEF push the request out to the network to be serviced by an external web server and require that the system has an active internet connection.


An alternative is to initialise the HTMLRenderer by setting its [URL](./url.md) property. This is typically  used to display external content , rather than content delivered from the workspace.


If neither [HTML](./html.md) nor [URL](./url.md) is set when the HTMLRenderer is created, it will generate an [HTTPRequest](./httprequest.md) event with a requested url of http://dyalog_root.


When the HTMLRenderer is displayed in its own window, the  window caption is set by an assignment to its [Caption](./caption.md) property. The window caption may subsequently change  when content is displayed  (typically  by the title tag in the html). The [Caption](./caption.md) property reports the current window caption.

#### Example
```apl
     ∇ Example;enc;Q;U;tw
[1]    'f'⎕WC'Form' 'HTMLRender'
[2]    f.(Coord Size)←'Pixel'(730 700)
[3]    'pco'⎕CY'dfns'
[4]    'f.l1'⎕WC'Label' 'Primes<100'(10 10)
[5]    'f.p'⎕WC'HTMLRenderer'('AsChild' 1)('Posn' 40 10)(270 200)
[6]    f.p.HTML←HTMLTable('*'@(0∘pco)10 10⍴⍳100)
[7]    Q←'Has the Large Hadron Collider destroyed the world yet?'
[8]    'f.l2'⎕WC'Label'Q(320 10)
[9]    'f.q'⎕WC'HTMLRenderer'('ASChild' 1)
[10]   f.q.(Posn Size)←(350 10)(360 360)
[11]   U←'http://hasthelargehadroncolliderdestroyedtheworldyet.com'
[12]   f.q.URL←U
[13]   tw←'<a class="twtimeline"'
[14]   tw,←'href="https://twitter.com/dyalogapl">'
[15]   tw,←'Tweets by dyalogapl</a>'
[16]   tw,←'<script async src="http://platform.twitter.com/widgets.js"'
[17]   tw,←'charset="utf-8"></script>'
[18]   'f.t'⎕WC'HTMLRenderer'('AsChild' 1)
[19]   f.t.(Posn Size)←(10 400)(680 280)
[20]   f.t.HTML←tw
     ∇

```
```apl

     enc←{'<',⍺,'>',(∊⍕⍵),'</',((~∨\' '=⍺)/⍺),'>'}
     
     HTMLTable←{'table border="1"'enc∊(⊂'tr')enc∘∊¨↓(⊂'td')enc¨⍵}
     

```


![htmlrenderer1](../img/htmlrenderer1.png)


