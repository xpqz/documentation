




<h1 class="heading"><span class="name">Group</span></h1>

| [Parents](../ParentLists/Group.htm) | [Children](../ChildLists/Group.htm) | [Properties](../PropLists/Group.htm) | [Methods](../MethodLists/Group.htm) | [Events](../EventLists/Group.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object is used to group a related set of controls together         visually, and to impose "radio-button" behaviour. |
| --- | ---  |


**Description**


A Group is displayed as an empty box with a border around it whose appearance
is defined by the [EdgeStyle](../a-z/edgestyle.md) property. The
[Caption](../a-z/caption.md) property defines a string of text
that is displayed in the top left border. The default value is an empty vector.



A Group will be resized if its parent [Form](../a-z/form.md) or
Group is resized. It can also be resized directly by the user if its [Sizeable](../a-z/sizeable.md) property is set to 1. By default, when a Group is resized, it automatically
adjusts the size and position of its children to maintain the same proportions
within it as before. The resizing of a Group and its children can be controlled
using the [AutoConf](../a-z/autoconf.md) property or by enabling
the [Configure](../a-z/configure.md) event (31).


