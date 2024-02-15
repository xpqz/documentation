




<h1 class="heading"><span class="name">FileBox</span></h1>

| [Parents](../ParentLists/FileBox.htm) | [Children](../ChildLists/FileBox.htm) | [Properties](../PropLists/FileBox.htm) | [Methods](../MethodLists/FileBox.htm) | [Events](../EventLists/FileBox.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Prompts user to select a file. |
| --- | ---  |


**Description**


The FileBox object implements the standard Windows FileSelection Dialog Box. This is a "modal" object. When you create a FileBox with [`⎕WC`](../../Language/System%20Functions/wc.htm), it is initially invisible and the user cannot interact with it. To use it, you must execute [`⎕DQ`](../../Language/System%20Functions/dq.htm) with the name of the FileBox as its right argument. This causes the FileBox to be displayed. During the "local" [`⎕DQ`](../../Language/System%20Functions/dq.htm) the user may interact **only** with the FileBox, or with other applications. When the user terminates the operation (by pressing the "Save", "Open", or "Cancel" Buttons, or by closing the window) the "local" [`⎕DQ`](../../Language/System%20Functions/dq.htm) terminates, and the FileBox disappears.



When the "local" [`⎕DQ`](../../Language/System%20Functions/dq.htm) is terminated, the FileBox generates either an [FileBoxOK](./fileboxok.md)(71) or [FileBoxCancel](./fileboxcancel.md)(72) event. The former is generated when the user presses the "Save" or "Open" button; the latter when the user presses the "Cancel" button or closes the FileBox.


The [FileMode](./filemode.md) property is a character vector which indicates the mode in which the selected file is going to be opened. [FileMode](./filemode.md) may be `'Read'` (the default) or `'Write'`. If [FileMode](./filemode.md) is `'Write'`, files listed in the File Selection Box are "greyed", although they may still be selected.


The [Caption](./caption.md) property determines the text that appears in the title bar of the FileBox window. If undefined, [Caption](./caption.md) defaults to "Save As" if [FileMode](./filemode.md) is `'Write'` or to "Open" if [FileMode](./filemode.md) is `'Read'`. Similarly, if [FileMode](./filemode.md) is `'Write'`, the button captions are "Save" and "Cancel", and if [FileMode](./filemode.md) is `'Read'` the button caption are "Open" and "Cancel".


The [Directory](./directory.md) property contains a simple character vector which specifies the initial directory from which a list of suitable files is displayed.
```apl
      'F' ⎕WC 'FileBox' 'The FileBox Object' 'C:\WDYALOG'
      ⎕DQ 'F'
```


The [Style](./style.md) property specifies whether the user may choose a single file name (`'Single'`  which is the default) or several file names (`'Multi')`.


The [Filters](./filters.md) property is a nested scalar or vector containing a list of filters. Each filter is a 2-element vector of character vectors which contain a file type mask and a file type description respectively. The file type descriptions appear in a drop-down combo box labelled "List File of Type". When the user selects one of these, the currently selected directory is searched for files which match the corresponding mask. The default value of [Filters](./filters.md) is an empty vector. This gives a file type mask of "*.*" and a file type description of "All Files (*.*)". Hence an empty vector is equivalent to `(⊂'*.*' 'All Files (*.*)').`


The [Index](./index.md) property determines which of the filters is initially selected. Its default value is `⎕IO`.


Note that when [`⎕DQ`](../../Language/System%20Functions/dq.htm) terminates with [FileBoxOK](./fileboxok.md), the [File](./file.md), [Directory](./directory.md), and [Index](./index.md) properties are updated to reflect the contents of the fields within the FileBox.


The operating system imposes limits on both the length of the name of the file, and on the total path length. In version attempting to set the `File` or `Directory` Properties to too long a name will generate a DOMAIN ERROR, while attempting to use too long a File name within the FileBox will result in the appearence of an error MessageBox.


