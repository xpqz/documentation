




<h1 class="heading"><span class="name">ColorButton</span></h1>

[Parents](../ParentLists/ColorButton.htm) [Properties](../PropLists/ColorButton.htm) [Methods](../MethodLists/ColorButton.htm) [Events](../EventLists/ColorButton.htm)


Purpose: The ColorButton object allows the user to select a colour.


**Description**


The ColorButton object displays a coloured box, with an optional drop down button. When the user clicks the ColorButton with the left mouse button, a colour selection drop-down appears below it, allowing the user to select a new colour.



The [CurrentColor](../a-z/currentcolor.md) property (default 0 0 0) is a 3-element integer vector that specifies and reports the RGB value of the currently selected colour.


The [DefaultColors](../a-z/defaultcolors.md) property is a nested matrix which specifies the RGB values of the colours shown in the colour selection box. The shape of [DefaultColors](../a-z/defaultcolors.md) determines the number of rows and columns in the colour selection drop-down. Each element of [DefaultColors](../a-z/defaultcolors.md) is a 3-element integer vector specifying an RGB colour value.


The [OtherButton](../a-z/otherbutton.md) property is Boolean and specifies whether or not the user can select a colour using the Windows colour selection dialog box.


If [OtherButton](../a-z/otherbutton.md) is 1 (the default), the final row of the colour selection drop-down contains a button labelled "Other…". If the user clicks this button, the standard Windows colour selection dialog box is displayed, allowing the user to select any colour that the computer can render.


If [OtherButton](../a-z/otherbutton.md) is 0, the button labelled "Other…" is not present and the user is restricted to the choice of colours provided by the [DefaultColors](../a-z/defaultcolors.md) property.


The [CustomColors](../a-z/customcolors.md) property is a 1-row, 16-column nested matrix which specifies the RGB values of the Colours displayed in the *Custom colors* section of the Windows colour selection dialog box. Each element of [CustomColors](../a-z/customcolors.md) is a 3-element integer vector specifying an RGB colour value.


The [ShowDropDown](../a-z/showdropdown.md) property is Boolean (default 1) and specifies whether or not a drop-down button is displayed in the ColorButton object.


When the user clicks a ColorButton with the left mouse button, the object generates a [DropDown](../a-z/dropdown.md) event just before it displays the colour selection drop-down. This event may be used to set the [DefaultColors](../a-z/defaultcolors.md) and/or [CustomColors](../a-z/customcolors.md) properties dynamically.


When the user selects a new colour, the ColorButton generates a [ColorChange](../a-z/colorchange.md) event.


Note that Pocket PC 2002 colour selection dialog box does not provide the facility to select *custom colours*, so this functionality is not available in PocketAPL.


