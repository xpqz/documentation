




<h1 class="heading"><span class="name">Button</span></h1>

[Parents](../ParentLists/Button.htm) [Children](../ChildLists/Button.htm) [Properties](../PropLists/Button.htm) [Methods](../MethodLists/Button.htm) [Events](../EventLists/Button.htm)


Purpose: Allows the user to initiate an action or to select an option using a button.


**Description**


The type of button displayed is determined by the [Style](./style.md) property which may take the value `'Push'`, `'Radio'`, `'Check'`, `'Toggle'`, `'Split'` or `'CommandLink'`. Under Windows, `'Toggle'` and `'Check'` are treated identically.



`'Split'` and `'CommandLink'` apply only to Windows Vista and later and require  [Native Look and Feel ](../../Miscellaneous/Windows XP Look and Feel.htm)
[(see page 1)](../../Miscellaneous/Windows XP Look and Feel.htm#Native_Look_and_Feel)
. Otherwise the use of these Styles will produce a Button with Style `'Push'`.


Push buttons are used to generate actions. When the user "presses" a pushbutton, it generates a [Select](./select.md) event (30). To cause an action, you simply associate the name of a callback function with this event for the Button in question.


Radio buttons and Check boxes are used to select options. They each have two states between which the user can toggle by clicking the mouse. When the Button (option) is selected, its [State](./state.md) property has the value 1; otherwise it is 0.


Only one of a group of Radio buttons which share the same parent can be set ([State](./state.md) is 1) at any one time. Radio buttons are therefore used for a set of choices that are **mutually exclusive**. Check boxes however, may be set together to signify a combination of options. These are used for making choices which are not mutually exclusive.


Radio and Check buttons **also** generate [Select](./select.md) events when their [State](./state.md) changes, and you can attach callback functions to these events to keep track of their settings. However, as Radio and Check buttons are not normally used to generate actions, it is perhaps easier to wait until the user signifies completion of the dialog box in some way, and then query the [State](./state.md) of the buttons using [`⎕WG`](../../Language/System Functions/wg.htm). For example, if you have a set of Radio or Check buttons in a [Group](group.md) called `f1.options`, the following statements retrieve their settings.
```apl
      OPTIONS ← (⎕WN 'f1.options') ⎕WG¨⊂'State'
```


or
```apl
      OPTIONS ← ⎕WG∘'State' ¨ ⎕WN 'f1.options'
```


The [Caption](./caption.md) property determines the text displayed in the Button. Its default value is an empty vector. If the [Caption](./caption.md) property contains one or more linefeed characters (`⎕UCS 10`) the text is centre-justifed ([Style](./style.md) `'Push'` only) or top-left justified and automatically wraps on white-space characters (such as space and tab) to fit in the width provided.


If [Style](./style.md) is `'Radio'` or `'Check'`, the text may be aligned to the left or right of the button graphic using the [Align](./align.md) property. Its default value is `'Right'`.


The CommandLink button has an icon displayed to the left of its [Caption](./caption.md). The appearance of the icon is controlled by the  [Elevated](./elevated.md) property. **Elevation** is a feature of **User Account Control** in Windows 7. In addition to the [Caption](./caption.md), additional text may be defined by its [Note](./note.md) property. If provided, this is displayed below the [Caption](./caption.md).


The Split [Button](button.md) has a drop-down button, similar to that provided by a [Combo](combo.md) object.


If [Posn](./posn.md) is omitted, the button is placed in the centre of its parent. If either element of [Posn](./posn.md) is set to `⍬`, the button is centred along the corresponding axis.


If [Size](./size.md) is not specified, the size of the button is determined by its [Caption](./caption.md). If either element of [Size](./size.md) is set to `⍬` the corresponding dimension is determined by the height or width of its [Caption](./caption.md). This does not apply to multi-line buttons whose dimensions should be specified explicity. If [Caption](./caption.md) is not specified, or is set to an empty vector, the value of [Size](./size.md) is set to a default value.


Button colours can be specified using [FCol](./fcol.md) and [BCol](./bcol.md). However, pushbuttons ([Style ](./style.md)`'Push'`) **ignore**[BCol](./bcol.md) and instead use the standard Windows colour.


The [Picture](./picture.md) property is used to display a bitmap on a pushbutton. This property is a 2-element array containing the name of a [Bitmap](bitmap.md) object and the "mode" in which it is to be displayed. The default mode (3) is the most useful, as it causes the [Bitmap](bitmap.md) to be **superimposed** on the centre of the Button. The surrounding edges of the Button (which gives it its 3-dimensional appearance and pushbutton behaviour) are unaffected. Note that if Picture is set on a Button whose Style is `'Radio'` or `'Check'`, the Button assumes pushbutton appearance, although its `'Radio'` /       `'Check'` behaviour is preserved.


An alternative is to use the [BtnPix](./btnpix.md) property. This property specifies the names of up to 3 [Bitmap](bitmap.md) objects. The first [Bitmap](bitmap.md) is displayed when the [State](./state.md) of the Button is 0. The second is displayed when its [State](./state.md) is 1. The third is shown when the Button is inactive ([Active](./active.md) 0). [BtnPix](./btnpix.md) is more flexible than [Bitmap](bitmap.md), but if you want your Button to exhibit pushbutton behaviour, you must design your bitmap accordingly.


The [ReadOnly](./readonly.md) property is Boolean and specifies whether or not the user may change the state of the Button. It applies only to [Style ](./style.md)`'Radio'` and [Style](./style.md) `'Check'`.


The user can interact with the [Button](button.md) by clicking it, which generates a [Select](./select.md) Event  or (Style `'Split'`) the drop-down which generates a [DropDown](./dropdown.md) Event.


