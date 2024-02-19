




<h1 class="heading"><span class="name">Border</span></h1>

**Applies To**


**Description**


This property specifies whether or not an object is displayed with a border around it. It is a single number with the value 0 (no border)1 (Border), or 2. The value 2 applies only to a [Form](../a-z/form.md) and is used in combination with `('EdgeStyle' 'Dialog')` to obtain standard dialog box appearance


For a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), the value of the Border property is only relevant if [Sizeable](../a-z/sizeable.md), [Moveable](../a-z/moveable.md), [SysMenu](../a-z/sysmenu.md), [MaxButton](../a-z/maxbutton.md) and [MinButton](../a-z/minbutton.md) are **all** 0.

#### Note


The value of the Border property may only be assigned by [`⎕WC`](../../Language/System Functions/wc.htm) and may **not** be changed using [`⎕WS`](../../Language/System Functions/ws.htm).



