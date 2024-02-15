




<h1 class="heading"><span class="name">Sizeable</span></h1>

**Applies To**


**Description**


This property determines whether or not an object can be directly resized by the user once it has been created by [`⎕WC`](../../Language/System%20Functions/wc.htm).



It is a single number with the value 0 (the object cannot be resized by the user) or 1 (the object may be resized by the user). The default is 1.


For a [Form](../a-z/form.md) , [HTMLRenderer](../a-z/htmlrenderer.md) or [SubForm](../a-z/subform.md), the Sizeable property may only be set by [`⎕WC`](../../Language/System%20Functions/wc.htm) and cannot subsequently be altered using [`⎕WS`](../../Language/System%20Functions/ws.htm). An attempt to do so generates a `NONCE ERROR`. For a [Form](../a-z/form.md) or [HTMLRenderer](../a-z/htmlrenderer.md), the default value is 1 and the object occupies a standard resizeable window with a border. Note that the value of Sizeable is independent of the values of the [MaxButton](../a-z/maxbutton.md) and [MinButton](../a-z/minbutton.md) properties, so that a [Form](../a-z/form.md) or [HTMLRenderer](../a-z/htmlrenderer.md) with [MaxButton](../a-z/maxbutton.md) 1 can be maximised even though its Sizeable property is 0.


For other objects, the default value of the Sizeable property is 0. However, setting it to 1 (which may be done dynamically using [`⎕WS`](../../Language/System%20Functions/ws.htm)) allows the user to resize it with the mouse.


In all these cases, when the user resizes an object, the object will generate a [Configure](../a-z/configure.md) (31) event.


Sizeable also applies to the [Locator](../a-z/locator.md) object. In this case, a value of 1 implies "rubberbanding" and a value of 0 means "no rubberbanding". See [Locator](../a-z/locator.md) object for further details.


