




<h1 class="heading"><span class="name">ButtonEdit</span></h1>

| [Parents](../ParentLists/ButtonEdit.htm) | [Children](../ChildLists/ButtonEdit.htm) | [Properties](../PropLists/ButtonEdit.htm) | [Methods](../MethodLists/ButtonEdit.htm) | [Events](../EventLists/ButtonEdit.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Allows user to enter or edit data. |
| --- | ---  |


**Description**


The ButtonEdit object combines a single-line input field with a customisable button. It provides the same user and programmer interfaces as an [Edit](../a-z/edit.md) object (Style `'Single'`).



The appearance of the button, which is displayed to the right of the input field, is determined by the [ImageListObj](../a-z/imagelistobj.md) property. When clicked, the object generates a [DropDown](../a-z/dropdown.md) event. There is no default processing for this event; it is up to the programmer to take the appropriate action via a callback function.


The following picture illustrates two ButtonEdit objects
```apl
     ∇ Example;BK;White;dyalog
[1]    dyalog←2 ⎕NQ'.' 'GetEnvironment' 'Dyalog'
[2]    'F'⎕WC'Form' 'ButtonEdit'('Coord' 'Pixel')('Size' 200 240)
[3]    'F'⎕WS'Coord' 'Pixel'
[4]    'F.IL1'⎕WC'ImageList'('Size' 16 16)('Masked' 1)
[5]    'F.IL1.Time'⎕WC'Icon'(dyalog,'\ws\arachnid.ico')
[6]    'F.BE1'⎕WC'ButtonEdit' ''(30 20)(⍬ 200)
[7]    F.BE1.(Cue ShowCueWhenFocused)←'Enter data' 1
[8]    F.BE1.(ImageListObj ImageIndex)←F.IL1 1
[9]
[10]   'F.fnt'⎕WC'Font' 'APL385 Unicode' 16
[11]   BK←16 16⍴256⊥White←255 255 255
[12]   'F.Rotate'⎕WC'Bitmap'('CBits'BK)('MaskCol'White)
[13]   'F.Rotate.'⎕WC'Text' '⌽'(0 3)('FontObj'F.fnt)
[14]   BK←F.Rotate.CBits
[15]   'F.IL1.'⎕WC'Bitmap'('CBits'BK)('MaskCol'White)
[16]   'F.BE2'⎕WC'ButtonEdit' 'Hello World'(100 20)(⍬ 200)
[17]   F.BE2.(ImageListObj ImageIndex)←F.IL1 2
[18]   F.BE2.onDropDown←'Rotate'
     ∇


     ∇ Rotate msg
[1]    (⊃msg).Text←⌽(⊃msg).Text
     ∇


```


![buttonedit](../img/buttonedit.png)

#### Note


For full functionality (in particular, for the [Cue](../a-z/cue.md) property to apply), the ButtonEdit object requires that  [Native Look and Feel ](../../Miscellaneous/Windows XP Look and Feel.htm)
(see page 1)
 is enabled.


