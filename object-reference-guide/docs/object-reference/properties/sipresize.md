




<h1 class="heading"><span class="name">SIPResize</span></h1>

Applies To: [Form](../a-z/form.md)


**Description**


**SIPResize applies only to PocketAPL. In versions of Dyalog APL for other platforms, it has no effect.**


This is a Boolean property that specifies the behaviour of a Form when the Input Panel is raised or lowered.


If SIPResize is 1 (the default), the [Form](../a-z/form.md) generates a Configure event when the Input Panel is raised or lowered. Unless disabled or modified by a callback function, the Form is automatically resized to occupy the entire space above the Input Panel.


If SIPResize is 0, the [Form](../a-z/form.md) does not generate a Configure event when the Input Panel is raised or lowered. This means that, at times, the lower part of the [Form](../a-z/form.md) may be obscured by the Input Panel.



