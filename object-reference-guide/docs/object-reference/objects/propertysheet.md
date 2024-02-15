




<h1 class="heading"><span class="name">PropertySheet</span></h1>

| [Parents](../ParentLists/PropertySheet.htm) | [Children](../ChildLists/PropertySheet.htm) | [Properties](../PropLists/PropertySheet.htm) | [Methods](../MethodLists/PropertySheet.htm) | [Events](../EventLists/PropertySheet.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The PropertySheet object represents a standard multi-page dialog box. |
| --- | ---  |


**Description**


There are two different kinds of PropertySheet which you select using the Style property. This may only be set when the PropertySheet is created using `⎕WC` and Style may not subsequently be changed using `⎕WS`.



If Style is Standard (the default), the PropertySheet displays a set of pages (each represented by a [PropertyPage](../a-z/propertypage.md)) as a set of tabbed forms as illustrated below. The user selects the current page by clicking on the appropriate tab. This Style allows the user to select any page at any time and does not oblige the user to visit any but the first page you choose to display. This Style is useful for displaying groups of options or settings that the user may change.


![ps1](../img/ps1.gif)


If Style is Wizard, the PropertySheet displays its pages in succession starting with the first. The user steps from one to another using the Next and Back buttons and may be forced to visit all the pages in a prescribed order. This Style is useful for data entry or for asking the user to make a series of choices.


![ps2](../img/ps2.gif)


The Caption property specifies the text written in the window title bar, but only applies if the Style is Standard. The title bar text of a Wizard PropertySheet is specified by the Caption of the current [PropertyPage](../a-z/propertypage.md).


The HasApply and HasHelp properties are Boolean and specify whether or not the PropertySheet has "Apply" and "Help" buttons respectively. These properties may only be set when the object is created using `⎕WC`. They both have default values of 1.


The FontObj and EdgeStyle properties have no effect on the appearance of the PropertySheet itself, but may be used to define the default appearance of its children.


