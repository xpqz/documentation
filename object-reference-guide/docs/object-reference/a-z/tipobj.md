




<h1 class="heading"><span class="name">TipObj</span></h1>

**Applies To**


**Description**


The TipObj property is a character vector or ref that specifies the name of, or ref to, a [TipField](./tipfield.md) object in which the "help" message defined by the [Tip](tip.md) property is to be displayed. This message is displayed when the user positions the mouse pointer over the object.


Note that if TipObj is empty, its value is inherited from its parent. Thus setting TipObj on a [Form](./form.md) defines the default [TipField](./tipfield.md) (and thus the default appearance of all [Tip](tip.md)s) for all the controls in that [Form](./form.md). Setting TipObj on [Root](./root.md) defines the default [TipField](./tipfield.md) for the entire application.



