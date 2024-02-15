




<h1 class="heading"><span class="name">Visible</span></h1>

**Applies To**


**Description**


This property specifies whether or not an object is currently visible. It is a single number with the value 0 (object is invisible) or 1 (object is visible). The default is 1. Setting Visible on and off is a way to pop a dialog box up and down as required.


Note that an invisible object is not necessarily inactive, and is capable of generating events. For example, a [Button](./button.md) with a [Cancel](cancel.md) property of 1 will generate a [Select](./select.md) (30) event (if enabled) whether or not it is visible. An invisible object will also respond to methods and  events sent to it by [`⎕NQ`](../../Language/System%20Functions/nq.htm).



