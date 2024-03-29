




<h1 class="heading"><span class="name">OKButton</span></h1>

Applies To: [Form](./form.md)


**Description**


This is a Boolean property that specifies whether or not an [OK] button appears in the title bar of a [Form](./form.md). Its default value is 0.



**OKButton applies only to PocketAPL. In versions of Dyalog APL for other platforms, it has no effect.**


OKButton may only be specified when the [Form](./form.md) is created using `⎕WC`; you cannot subsequently change its value.


If OKButton is 1, the [Form](./form.md) displays an [OK]  button in its title bar in place of the standard [X] button.


When the user clicks the [OK] button, the system will press the default button, which is specified by the [Default](default.md) property of a [Button](./button.md) on the [Form](./form.md).


If there is no default button, the [Form](./form.md) will generate a [Close](./close.md) event.


