




<h1 class="heading"><span class="name">Border</span></h1>

**Applies To**


**Description**


This property specifies whether or not an object is displayed with a border around it. It is a single number with the value 0 (no border)1 (Border), or 2. The value 2 applies only to a [Form](./form.md) and is used in combination with `('EdgeStyle' 'Dialog')` to obtain standard dialog box appearance


For a [Form](./form.md) or [SubForm](./subform.md), the value of the Border property is only relevant if [Sizeable](sizeable.md), [Moveable](moveable.md), [SysMenu](sysmenu.md), [MaxButton](maxbutton.md) and [MinButton](minbutton.md) are **all** 0.

#### Note


The value of the Border property may only be assigned by [`⎕WC`](../../Language/System%20Functions/wc.htm) and may **not** be changed using [`⎕WS`](../../Language/System%20Functions/ws.htm).



