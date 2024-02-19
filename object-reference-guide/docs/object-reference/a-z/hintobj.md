




<h1 class="heading"><span class="name">HintObj</span></h1>

**Applies To**


**Description**


The HintObj property is a character vector or ref that specifies the name of, or a ref to, an object in which the "help" message defined by the [Hint](Hint.htm) property is to be displayed. This message is displayed when the user positions the mouse pointer over the object. The [Hint](Hint.htm) is displayed by automatically setting the [Caption](Caption.htm) or [Text](Text.htm) property of the object named by HintObj.


The following types of object can therefore be used to display Hints: [Button](./button.md), [Edit](./edit.md), [Combo](./combo.md), [Group](./group.md), [Form](./form.md), [Label](./label.md), [Menu](./menu.md), [MenuItem](./menuitem.md), [StatusField](./statusfield.md), [SubForm](./subform.md) and [Text](./text.md). For a [StatusField](./statusfield.md) that has both [Caption](Caption.htm) and [Text](Text.htm) properties, the text property is used for displaying hints.


When the user moves the mouse pointer away from the object, the [Caption](Caption.htm) or [Text](Text.htm) property of the object specified by HintObj is reset to an empty vector.


Note that if HintObj is empty, its value is inherited from its parent. Thus setting HintObj on a [Form](./form.md) defines the default location for displaying [Hint](Hint.htm)s for all the controls in that [Form](./form.md). Setting HintObj on [Root](./root.md) defines the default location for hints for the entire application.



