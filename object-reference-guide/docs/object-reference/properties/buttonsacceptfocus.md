




<h1 class="heading"><span class="name">ButtonsAcceptFocus</span></h1>

Applies To: [ToolControl](../a-z/toolcontrol.md)


**Description**


This is a Boolean property that determines how the Tab key and other cursor movement keys are handled by a [ToolControl](../a-z/toolcontrol.md) object.


If ButtonsAcceptFocus is 0 (the default), when the user presses Tab or Shift+Tab to switch the input focus from another object to the [ToolControl](../a-z/toolcontrol.md), the first [ToolButton](../a-z/toolbutton.md) in the [ToolControl](../a-z/toolcontrol.md) receives the input focus and is highlighted. Pressing Tab or Shift+Tab again causes the input focus to move to another control. The cursor movement keys have no effect.


If ButtonsAcceptFocus is 1, when the user presses Tab or Shift+Tab to switch the input focus from another object to the [ToolControl](../a-z/toolcontrol.md), the first or last [ToolButton](../a-z/toolbutton.md) in the [ToolControl](../a-z/toolcontrol.md) receives the input focus and is highlighted. Note that the behaviour of Shift+Tab in this case is different. Pressing Tab or Shift+Tab again causes the input focus to move to another control, although if there is no other control to accept the input focus, it moves to the first or last [ToolButton](../a-z/toolbutton.md) as appropriate. Pressing the cursor movement keys causes the input focus to move from one [ToolButton](../a-z/toolbutton.md) to the next.



