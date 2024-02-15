




<h1 class="heading"><span class="name">OKButton</span></h1>
| Applies To: | [Form](../a-z/form.md) |
| --- | ---  |

| Applies To: | [Form](../a-z/form.md) | [Form](../a-z/form.md) |  |  |
| --- | --- | ---  |
| [Form](../a-z/form.md) |  |  |


Description


This is a Boolean property that specifies whether or not an [OK] button appears in the title bar of a [Form](../a-z/form.md). Its default value is 0.



OKButton applies only to PocketAPL. In versions of Dyalog APL for other platforms, it has no effect.


OKButton may only be specified when the [Form](../a-z/form.md) is created using `⎕WC`; you cannot subsequently change its value.


If OKButton is 1, the [Form](../a-z/form.md) displays an [OK]  button in its title bar in place of the standard [X] button.


When the user clicks the [OK] button, the system will press the default button, which is specified by the [Default](../a-z/default.md) property of a [Button](../a-z/button.md) on the [Form](../a-z/form.md).


If there is no default button, the [Form](../a-z/form.md) will generate a [Close](../a-z/close.md) event.


