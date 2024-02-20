




<h1 class="heading"><span class="name">MaxButton</span></h1>

Applies To: [Form](./form.md) [HTMLRenderer](./htmlrenderer.md) [SubForm](./subform.md)


**Description**


This property determines whether or not an object has a "maximise" button. Pressing this button will cause a [Form](./form.md) or [HTMLRenderer](./htmlrenderer.md) to be resized to occupy the entire screen, or a [SubForm](./subform.md) to occupy the entire area of its parent. Pressing it again will restore the object to its original size. MaxButton is a single number with the value 0 (no maximise button) or 1 (maximise button is provided). The default is 1.


Note that MaxButton is independent of [Sizeable](sizeable.md), i.e. you can define an object that can be maximised but not resized. If any of the properties MaxButton, [MinButton](minbutton.md), [SysMenu](sysmenu.md) and [Sizeable](sizeable.md) are set to 1, the object will have a title bar.



