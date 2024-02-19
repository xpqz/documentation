




<h1 class="heading"><span class="name">Button</span></h1>

| [Parents](../ParentLists/Button.htm) | [Children](../ChildLists/Button.htm) | [Properties](../PropLists/Button.htm) | [Methods](../MethodLists/Button.htm) | [Events](../EventLists/Button.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Allows the user to initiate an action or to select an option using a button. |
| --- | ---  |


**Description**


The type of button displayed is determined by the [Style](../a-z/style.md) property which may take the value `'Push'`, `'Radio'`, `'Check'`, `'Toggle'`, `'Split'` or `'CommandLink'`. Under Windows, `'Toggle'` and `'Check'` are treated identically.



`'Split'` and `'CommandLink'` apply only to Windows Vista and later and require  [Native Look and Feel ](../../Miscellaneous/Windows XP Look and Feel.htm)
(see page 1)
. Otherwise the use of these Styles will produce a Button with Style `'Push'`.


Push buttons are used to generate actions. When the user "presses" a pushbutton, it generates a [Select](../a-z/select.md) event (30). To cause an action, you simply associate the name of a callback function with this event for the Button in question.


Radio buttons and Check boxes are used to select options. They each have two states between which the user can toggle by clicking the mouse. When the Button (option) is selected, its [State](../a-z/state.md) property has the value 1; otherwise it is 0.


Only one of a group of Radio buttons which share the same parent can be set ([State](../a-z/state.md) is 1) at any one time. Radio buttons are therefore used for a set of choices that are **mutually exclusive**. Check boxes however, may be set together to signify a combination of options. These are used for making choices which are not mutually exclusive.


Radio and Check buttons **also** generate [Select](../a-z/select.md) events when their [State](../a-z/state.md) changes, and you can attach callback functions to these events to keep track of their settings. However, as Radio and Check buttons are not normally used to generate actions, it is perhaps easier to wait until the user signifies completion of the dialog box in some way, and then query the [State](../a-z/state.md) of the buttons using [`⎕WG`](../../Language/System Functions/wg.htm). For example, if you have a set of Radio or Check buttons in a [Group](../a-z/group.md) called `f1.options`, the following statements retrieve their settings.
```apl
      OPTIONS ← (⎕WN 'f1.options') ⎕WG¨⊂'State'
```


or
```apl
      OPTIONS ← ⎕WG∘'State' ¨ ⎕WN 'f1.options'
```


The [Caption](../a-z/caption.md) property determines the text displayed in the Button. Its default value is an empty vector. If the [Caption](../a-z/caption.md) property contains one or more linefeed characters (`⎕UCS 10`) the text is centre-justifed ([Style](../a-z/style.md) `'Push'` only) or top-left justified and automatically wraps on white-space characters (such as space and tab) to fit in the width provided.


If [Style](../a-z/style.md) is `'Radio'` or `'Check'`, the text may be aligned to the left or right of the button graphic using the [Align](../a-z/align.md) property. Its default value is `'Right'`.


The CommandLink button has an icon displayed to the left of its [Caption](../a-z/caption.md). The appearance of the icon is controlled by the  [Elevated](../a-z/elevated.md) property. **Elevation** is a feature of **User Account Control** in Windows 7. In addition to the [Caption](../a-z/caption.md), additional text may be defined by its [Note](../a-z/note.md) property. If provided, this is displayed below the [Caption](../a-z/caption.md).


The Split [Button](../a-z/button.md) has a drop-down button, similar to that provided by a [Combo](../a-z/combo.md) object.


If [Posn](../a-z/posn.md) is omitted, the button is placed in the centre of its parent. If either element of [Posn](../a-z/posn.md) is set to `⍬`, the button is centred along the corresponding axis.


If [Size](../a-z/size.md) is not specified, the size of the button is determined by its [Caption](../a-z/caption.md). If either element of [Size](../a-z/size.md) is set to `⍬` the corresponding dimension is determined by the height or width of its [Caption](../a-z/caption.md). This does not apply to multi-line buttons whose dimensions should be specified explicity. If [Caption](../a-z/caption.md) is not specified, or is set to an empty vector, the value of [Size](../a-z/size.md) is set to a default value.


Button colours can be specified using [FCol](../a-z/fcol.md) and [BCol](../a-z/bcol.md). However, pushbuttons ([Style ](../a-z/style.md)`'Push'`) **ignore**[BCol](../a-z/bcol.md) and instead use the standard Windows colour.


The [Picture](../a-z/picture.md) property is used to display a bitmap on a pushbutton. This property is a 2-element array containing the name of a [Bitmap](../a-z/bitmap.md) object and the "mode" in which it is to be displayed. The default mode (3) is the most useful, as it causes the [Bitmap](../a-z/bitmap.md) to be **superimposed** on the centre of the Button. The surrounding edges of the Button (which gives it its 3-dimensional appearance and pushbutton behaviour) are unaffected. Note that if Picture is set on a Button whose Style is `'Radio'` or `'Check'`, the Button assumes pushbutton appearance, although its `'Radio'` /       `'Check'` behaviour is preserved.


An alternative is to use the [BtnPix](../a-z/btnpix.md) property. This property specifies the names of up to 3 [Bitmap](../a-z/bitmap.md) objects. The first [Bitmap](../a-z/bitmap.md) is displayed when the [State](../a-z/state.md) of the Button is 0. The second is displayed when its [State](../a-z/state.md) is 1. The third is shown when the Button is inactive ([Active](../a-z/active.md) 0). [BtnPix](../a-z/btnpix.md) is more flexible than [Bitmap](../a-z/bitmap.md), but if you want your Button to exhibit pushbutton behaviour, you must design your bitmap accordingly.


The [ReadOnly](../a-z/readonly.md) property is Boolean and specifies whether or not the user may change the state of the Button. It applies only to [Style ](../a-z/style.md)`'Radio'` and [Style](../a-z/style.md) `'Check'`.


The user can interact with the [Button](../a-z/button.md) by clicking it, which generates a [Select](../a-z/select.md) Event  or (Style `'Split'`) the drop-down which generates a [DropDown](../a-z/dropdown.md) Event.


