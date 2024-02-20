




<h1 class="heading"><span class="name">ActiveXControl</span></h1>

[Parents](../ParentLists/ActiveXControl.htm) [Children](../ChildLists/ActiveXControl.htm) [Properties](../PropLists/ActiveXControl.htm) [Methods](../MethodLists/ActiveXControl.htm) [Events](../EventLists/ActiveXControl.htm)


Purpose: The ActiveXControl object represents a Dyalog APL namespace as an ActiveX control.


**Description**



The ActiveXControl object represents a Dyalog APL namespace as an ActiveX control.


During development, an ActiveXControl is a container object that is the child of a Form and acts as a wrapper for one or more other GUI objects.


To make an ActiveXControl available to another application, you must select *Make OCX* from the Session *File* menu. This creates an .OCX file that contains your entire workspace and all of the ActiveXControls within it.


Once an ActiveXControl has been saved in an .OCX file, any application that supports ActiveX may create and use instances of it.


When an ActiveX control is loaded by a host application, it and any code that it requires, is loaded into the host application's address space; it does not run in a separate address space.


During development, an ActiveXControl is powered by the development version of Dyalog APL. However, an ActiveXControl object that is loaded by a host application, is powered by a DLL version of Dyalog APL. This automatically gets loaded when a host application creates the first instance of any Dyalog APL ActiveX control. However, within a single host application, other instances of the same or other Dyalog APL ActiveX controls share the same copy of DYALOG.DLL.


Like the development and run-time versions of Dyalog APL, DYALOG.DLL has an active workspace. When an application loads an ActiveXControl, DYALOG.DLL *copies* the *top-level namespace* that owns the ActiveXControl, together with everything it contains, into the active workspace. For example, if the ActiveXControl is named `Controls.Form1.Ctrl1`, the act of creating the first instance of `Ctrl1` will cause the entire contents of the `Controls` namespace to be copied, from the corresponding .OCX file, into the active workspace. This affords the potential for controls from different OCX files to clash, but the name clash conflict is restricted to just one name.


Each instance of an ActiveXControl, is represented by a separate namespace which is automatically *cloned* from the original ActiveXControl namespace. Each instance namespace is entirely separate from any other instance namespace and there is no way for one instance to reference or *see* any other instance; nor can it reference the original class namespace from which it was cloned. In fact, each instance appears to itself to be the one and only original class namespace. Using the previous example, each instance of `Ctrl1` believes that its full pathname is `#.Controls.Form1.Ctrl1`, although each instance is in fact a separate clone of that namespace.


When an application creates an instance of an ActiveXControl, it does so as the child of some object within its own GUI hierarchy. From the instance's viewpoint, its parent Form is replaced by a different GUI object that imposes position, size, font, background colour, and other ambient properties.


The external name of an ActiveXControl is made up of the character vector defined by the [ClassName](../a-z/classname.md) property, prefixed by the string "Dyalog ", and followed by the string " Control". If [ClassName](../a-z/classname.md) is empty (which is the default), the name of the ActiveXControl namespace is inserted instead. Note that the name should not include APL symbols such as `∆`.[ClassName](../a-z/classname.md) may only be specified when you create the ActiveXControl with `⎕WC` and may not be changed using `⎕WS`.


The [Coord](../a-z/coord.md) property is read-only and its value is always `'Pixel'`. If you wish to use a different co-ordinate system for the children of an ActiveXControl object, it is necessary to set [Coord](../a-z/coord.md) separately on each one of them.


[Posn](../a-z/posn.md) and [Size](../a-z/size.md) are negotiable properties. When an instance of the ActiveXControl is created, the values of [Posn](../a-z/posn.md) and [Size](../a-z/size.md) will be assigned by the host application. You may change these values using `⎕WS`, but the host application has the right to refuse them and there is no guarantee that you will get what you set.


The [Border](../a-z/border.md) and [EdgeStyle](../a-z/edgestyle.md) properties may be used to control the outline appearance of the ActiveXControl object.


The [Dragable](../a-z/dragable.md) and [KeepOnClose](../a-z/keeponclose.md) properties apply only during development and are otherwise ignored.


The [ToolboxBitmap](../a-z/toolboxbitmap.md) property specifies the name of a [Bitmap](../a-z/bitmap.md) object that may be used by a host application to represent the ActiveXControl when its complete visual appearance is not required.. For example, if you add an ActiveX control to the Microsoft Visual Basic development environment, its bitmap is added to the toolbox. The Bitmap should therefore be of an appropriate size, usually 24 x 24 pixels.


The [Container](../a-z/container.md) property provides access to an [ActiveXContainer](../a-z/activexcontainer.md) object that represents the host application itself. This may be used to obtain the values of ambient properties, or to access methods exposed by the host application via OLE interfaces.


When an instance of an ActiveXControl is created, it generates first a [PreCreate](../a-z/precreate.md) event, and then a Create event. The [PreCreate](../a-z/precreate.md) event is generated at the point the *instance* is made.


The [Create](../a-z/create.md) event is generated at the point when the host application requires the instance to appear visually. If, as is recommended, you create child controls of the instance when it is created, you must respond to the [Create](../a-z/create.md) event, because at the time that [PreCreate](../a-z/precreate.md) is generated, the object does not have a window.


Host applications which support two different modes of operation, namely design mode and run mode, differ in the way that they create instances of ActiveX controls. Microsoft Access does not require an ActiveX control to appear properly in design mode. Instead, it draws a simple box containing just the name of the object. If your ActiveXControl is hosted by Microsoft Access, it will get a [PreCreate](../a-z/precreate.md) Event when an instance is created in design mode, and a [Create](../a-z/create.md) event only when it enters run mode. Microsoft Visual Basic, however, requires the object to draw itself immediately, even in design mode, and so a [Create](../a-z/create.md) event will be generated immediately after a [PreCreate](../a-z/precreate.md) event in this case.


