




<h1 class="heading"><span class="name">StatusField</span></h1>

| [Parents](../ParentLists/StatusField.htm) | [Children](../ChildLists/StatusField.htm) | [Properties](../PropLists/StatusField.htm) | [Methods](../MethodLists/StatusField.htm) | [Events](../EventLists/StatusField.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object is used to display information for the user. |
| --- | ---  |


**Description**


The StatusField object provides an area for displaying context sensitive help messages, keyboard status, and other application dependent information.



By default a StatusField is a recessed rectangle in which information is displayed. It has a [Caption](../a-z/caption.md) and a [Text](../a-z/text.md) property, which by default are empty, but either or both of which can be used to present information. The [Caption](../a-z/caption.md) is left justified in the field and the [Text](../a-z/text.md) is displayed immediately to its right. Typically, you would use the [Caption](../a-z/caption.md) property as a title to describe the information that the StatusField displays, and the [Text](../a-z/text.md) property to show its current value. However, you are not obliged to use both of them and you can achieve most effects with just one.


Note that when the StatusField is used to display hints it is its [Text](../a-z/text.md) property that is used.


A StatusField may be used to monitor the status of the keyboard and this is controlled by its [Style](../a-z/style.md) property. The default value for [Style](../a-z/style.md) is an empty vector. However, you can set it to monitor various keyboard states as follows :


In each case, the [Text](../a-z/text.md) property of the StatusField is used to display the keyboard status. If [Style](../a-z/style.md) is CapsLock, ScrollLock or NumLock, the field displays "Caps", "Num" or "Scroll" if the corresponding mode is selected and is blank if not.


If  [Style](../a-z/style.md) is InsRep, the StatusField displays either "Ins" or "Rep". Initially it always displays "Ins" and then toggles between "Rep" and "Ins" each time the Insert key is pressed.


If [Style](../a-z/style.md) is KeyMode, the StatusField displays the name for the current keyboard mode which is defined in the input table being used. For the 2-mode tables APL_US.DIN, APL_UK.DIN etc., the mode name displayed is either "Apl" or "Asc".  The unified tables have no modes so a StatusField with this [Style](../a-z/style.md) does nothing.


If [Style](../a-z/style.md) is set to one of the above, you may still use the [Caption](../a-z/caption.md) property to give the StatusField a title. You may even set the value of the [Text](../a-z/text.md) property, but be aware that this value will be reset when the user next presses the key the StatusField is monitoring.


| CapsLock | Monitors state of Caps Lock key |
| --- | ---  |
| ScrollLock | Monitors state of Scroll Lock key |
| NumLock | Monitors state of Num Lock key |
| KeyMode | Monitors the keyboard mode (APL/ASCII) |
| InsRep | Monitors the state of the Insert key |


