




<h1 class="heading"><span class="name">Changed</span></h1>

| Applies To: | [ButtonEdit](../a-z/buttonedit.md) | [Edit](../a-z/edit.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Spinner](../a-z/spinner.md) |
| --- | --- | --- | --- | --- | ---  |


**Description**


The Changed property, in conjunction with the Change event, provides the means to control the validation of an object after the user has finished interacting with it.



Initially, the value of the Changed property of an object is set to 0. When the user gives the focus to the object and causes either the Text or (in the case of a [Spinner](../a-z/spinner.md)) the Thumb property to be altered, the Changed property is immediately set to 1. When the object loses the input focus and the value of the Changed property is 1, the object generates a Change event. The value of the Changed property is then determined as follows:


If there is no callback function attached to the Change event, or if the Change event is disabled, the Changed property is reset to 0.


If an attached callback returns no result or returns 1, the Change property is reset to 0.


If an attached callback function returns 0, the Changed property is not altered and remains set to 1. The object will therefore generate another Change event when the user next tries to leave it, even if the text and/or Thumb are not altered this time.


Note that the object generates a Change event when it loses the focus *only* if the value of the Changed property is 1 at the time.


