




<h1 class="heading"><span class="name">MinButton</span></h1>

Applies To: [Form](./form.md) [HTMLRenderer](./htmlrenderer.md) [SubForm](./subform.md)


**Description**


This property determines whether or not an object has a "minimise" button. Pressing this button will cause the object to be iconified. Pressing it again will restore the object to its original size. MinButton is a single number with the value 0 (no minimise button) or 1 (minimise button is provided). The default is 1.


Note that MinButton is independent of [Sizeable](sizeable.md), i.e. you can define an object that can be minimised but not resized.


If any of the properties MinButton, [MaxButton](maxbutton.md), [SysMenu](sysmenu.md), and [Moveable](moveable.md) are set to 1, the object will have a title bar.



