




<h1 class="heading"><span class="name">TabControl</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The TabControl object provides access to the native Windows tab         control. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Children | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Properties | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Methods | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| Events | [Detach](./detach.md) [GetTextSize](./gettextsize.md) [Animate](./animate.md) [GetFocus](./getfocus.md) [ShowSIP](./showsip.md) [GetFocusObj](./getfocusobj.md) | [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) | [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |
| [Detach](./detach.md) | [GetTextSize](./gettextsize.md) | [Animate](./animate.md) |
| [GetFocus](./getfocus.md) | [ShowSIP](./showsip.md) | [GetFocusObj](./getfocusobj.md) |


Description


The standard tab control is analogous to a set of dividers in a notebook and
allows you to define a set of *pages* that occupy the same area of a window
or dialog box. Each page consists of a set of information or a group of controls
that the application displays when the user selects the corresponding tab.



A special type of tab control displays tabs that look like buttons. For
example, the Windows taskbar is such a tab control.


The overall appearance of the TabControl is determined by the [Style](./style.md) property which may be `'Tabs'` (the
default), `'Buttons'` or `'FlatButtons'`.


Individual tabs or buttons are represented by TabButton objects which should be created as children of the TabControl object. Optional
captions and pictures are specified by the [Caption](./caption.md) and [ImageIndex](./imageindex.md) properties of the
individual TabButton objects themselves.
Otherwise, the appearance of the tabs or buttons is determined by properties of
the TabControl itself.


To implement a multiple page tabbed dialog (see Example 1), you should create a Form, then a
TabControl with Style `'Tabs'` as a child of
the Form. Next, create one or more pairs of TabButton and [SubForm](subform.md) objects as children of the
TabControl. You associate each [SubForm](subform.md) with a
particular tab by setting its [TabObj](./tabobj.md) property to the name of, or ref to, the associated TabButton object. Making the [SubForms](subform.md) children of the
TabControl ensures that, by default, they will automatically be resized
correctly. You may alternatively create your [SubForms](subform.md) as children of the main Form and establish
appropriate resize behaviour using their [Attach](./attach.md) property.


A TabControl object with [Style](./style.md) `'Buttons'` (Example 2) or `'FlatButtons'` (Example 3) may be used in a similar
way (i.e. to display a set of alternative pages), although buttons in this type
of TabControl are more normally used to execute commands. For this reason, these
styles of TabControl are without borders.


If [Style](./style.md) is `'FlatButtons'`,
the [FlatSeparators](./flatseparators.md) property
specifies whether or not separators are drawn between the buttons. The default
value of [FlatSeparators](./flatseparators.md) is 0 (no
separators).


Example 3a shows the
effect of setting [FlatSeparators](./flatseparators.md) to
1.


The [Align](./align.md) property specifies along which
of the 4 edges of the TabControl the tabs or buttons are arranged. [Align](./align.md) also controls the relative positioning of the picture and Caption within each
TabButton. [Align](./align.md) may be Top (the default),
Bottom, Left or Right.


If [Align](./align.md) is `'Top'` or `'Bottom'` (Example
4), the tabs or buttons are arranged along the top or bottom edge of the
TabControl and picture is drawn to the left of the Caption.


If [Align](./align.md) is `'Left'` (Example 5), the tabs or buttons are
arranged top-to-bottom along the left edge of the TabControl, and the pictures
are drawn below the Captions.


[In recent versions of Windows, ](./align.md)`'Align' 'Right'` fails to show the tabs or buttons on the right hand edge of the TabControl; this appears to be a limitation of Windows.


The [Attach](./attach.md) property specifies how the
TabControl responds when its parent is resized. Its default value, which is
independent of the [Align](./align.md) property, is `'None'
'None' 'None' 'None'`. This causes the TabControl to maintain its
original proportions when its parent is resized.


The [MultiLine](./multiline.md) property determines
whether or not your tabs or buttons will be arranged in multiple flights or
multiple rows/columns.


The default value of [MultiLine](./multiline.md) is 0,
in which case, if you have more tabs or buttons than will fit in the space
provided, the TabControl displays an UpDown control to permit the user to scroll
them. See Example 7.


If [MultiLine](./multiline.md) is set to 1, the tabs are
displayed in multiple flights (Example 8) or the buttons are displayed in multiple rows (Example
9).


The [ScrollOpposite](./scrollopposite.md) property
specifies that unneeded tabs scroll to the opposite side of a TabControl, when a
tab is selected. Setting [ScrollOpposite](./scrollopposite.md) to 1 forces [MultiLine](./multiline.md) to 1 also.


Example 10 illustrates a
TabControl with [ScrollOpposite](./scrollopposite.md) set
to 1, after the user has clicked *Third Tab*. Notice that, in this example,
the SubForms have been created as children of the TabControl. This is necessary
to ensure that they are managed correctly in this case.


If [MultiLine](./multiline.md) is 1, the way that
multiple flights of tabs or rows/columns of buttons are displayed is further
defined by the Justify property which may be `'Right'` (the default) or `'None'`.


If [Justify](./justify.md) is `'Right'`(which is the default), the TabControl increases the width of each tab, if
necessary, so that each row of tabs fills the entire width of the tab control.
Otherwise, if [Justify](./justify.md) is empty or `'None'`,
the rows are ragged.


See Example 11 (for tabs) and Example 12 (for
buttons).


By default, the size of the tabs may vary from one to another. Fixed size
tabs may be obtained by setting the [TabSize](./tabsize.md) property.


To obtain fixed sized tabs with [MultiLine](./multiline.md) set to 1, you must however also set Justify to `'None'`.


If fixed size tabs are in effect, the positions at which the picture and
Caption are drawn within each TabButton is
controlled by the [TabJustify](./tabjustify.md) property
which may be `'Centre'`, `'Edge'`,
or `'IconEdge'`.


Example
13 illustrates these different settings.


The font used to draw the captions in the TabButton objects is determined by the [FontObj](./fontobj.md) property of the TabControl.


You cannot specify the foreground or background colours of the tabs/buttons,
nor can you use different fonts in different tabs/buttons. The orientation of
the Caption text is always determined by the value of the Align property of the
TabControl.


The [TabObj](./tabobj.md) property is read-only and
reports the name of, or ref to, the TabButton that is currently selected.


The [MultiSelect](./multiselect.md) property specifies
whether or not the user can select more than one button in a TabControl at the
same time, by holding down the Ctrl key when clicking. The default is 0 (only
one button may be selected). [MultiSelect](./multiselect.md) is ignored if Style is `'Tabs'`.


The [TabFocus](./tabfocus.md) property specifies the
focus behaviour for the TabControl object and may be `'Normal'` (the
default), `'Never'` or `'ButtonDown'`.


The [HotTrack](./hottrack.md) property specifies whether
or not the tabs or buttons are automatically highlighted by the mouse pointer.
The default is 0 (no highlighting).


Note that the icons used in this example are provided in the ws sub-directory.
```apl
icodir←(2 ⎕NQ'.' 'GetEnvironment' 'Dyalog'),'\ws\'
```
```apl
'F'⎕WC'Form' 'TabControl: Default'('Size' 25 50)
'F.TC'⎕WC'TabControl'

'F.TC.IL'⎕WC'ImageList'
'F.TC.IL.'⎕WC'Icon'(icodir,'aplicon.ico')
'F.TC.IL.'⎕WC'Icon'(icodir,'funicon.ico')
'F.TC.IL.'⎕WC'Icon'(icodir,'editicon.ico')

'F.TC'⎕WS'ImageListObj' 'F.TC.IL'

'F.TC.T1'⎕WC'TabButton' 'One'('ImageIndex' 1)
'F.TC.T2'⎕WC'TabButton' 'Two'('ImageIndex' 2)
'F.TC.T3'⎕WC'TabButton' 'Three'('ImageIndex' 3)

'F.TC.S1'⎕WC'SubForm'('TabObj' 'F.TC.T1')
'F.TC.S2'⎕WC'SubForm'('TabObj' 'F.TC.T2')
'F.TC.S3'⎕WC'SubForm'('TabObj' 'F.TC.T3')
```


![tab1](../img/tab1.gif)


