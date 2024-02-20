




<h1 class="heading"><span class="name">ReadOnly</span></h1>

Applies To: [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Edit](../a-z/edit.md) [Spinner](../a-z/spinner.md)


**Description**


This property specifies whether or not the user may alter the text in an object. The default value of ReadOnly is 0 which allows the user to alter text.


If you set ReadOnly to 1, a cursor is displayed in the object, the user may navigate around the text in the usual manner with the mouse and/or the keyboard and select text and copy it to the clipboard. However, all input that would otherwise change the data is ignored.


For a Button object with [Style](../a-z/style.md) `'Radio'` or `'Check'`, setting ReadOnly to 1 prevents the user from changing the state of the [Button](../a-z/button.md), although mouse and other events will still be reported.



