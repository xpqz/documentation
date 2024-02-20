




<h1 class="heading"><span class="name">Grid</span></h1>

[Parents](../ParentLists/Grid.htm) [Children](../ChildLists/Grid.htm) [Properties](../PropLists/Grid.htm) [Methods](../MethodLists/Grid.htm) [Events](../EventLists/Grid.htm)


Purpose: Spreadsheet object for displaying and editing data.


**Description**


The [Values](../a-z/values.md) property is a matrix whose
elements are displayed in the cells of the Grid. An element (and therefore a
cell) may contain a single number, a single character, a character vector or a
character matrix.



The [CellHeights](../a-z/cellheights.md) property specifies
the height of each of the rows of the spreadsheet. It may be a single value
which applies to all rows, or a vector with one element per row. The [CellWidths](../a-z/cellwidths.md) property determines the width of each column of the spreadsheet. It too may be a
single value or a vector with one element per column.


The [RowTitles](../a-z/rowtitles.md) property is either an
empty character vector (the default) or a vector of character vectors that
specify row titles displayed to the left of the cells in the Grid. If [RowTitles](../a-z/rowtitles.md) is not specified, the Grid labels each row with its row number. The [ColTitles](../a-z/coltitles.md) property is similar and is used to specify column headings. If [ColTitles](../a-z/coltitles.md) is not specified, the Grid displays "standard" spreadsheet column headings
A-Z, then AA-AZ and so forth.


The [TitleHeight](../a-z/titleheight.md) property specifies
height of the column headers. If this is set to 0, the column titles will not be
displayed. Similarly, the [TitleWidth](../a-z/titlewidth.md) property specifies the width of the row titles and again a value of zero
disables the row titles.


The [CornerTitleBCol](../a-z/align.md) property specifies the background colour of the rectangle in the top-left corner of the Grid.


The [FontObj](../a-z/fontobj.md) property may be used to
specify the font to be used for the Grid as a whole, including the titles. The [CellFonts](../a-z/cellfonts.md) property may be used to specify fonts for individual cells.


The [FCol](../a-z/fcol.md) and [BCol](../a-z/bcol.md) properties may each specify a single colour for the Grid as a whole, or may
specify a vector of colours whose elements are mapped to individual cells
through the [CellTypes](../a-z/celltypes.md) property.


The [CellFonts](../a-z/cellfonts.md) property is either a
character vector or a vector of character vectors that specifies the name of a
single font object to be used for all cells in the Grid, or a vector of
character vectors that specifies a set of font objects that are mapped to
individual cells through the [CellTypes](../a-z/celltypes.md) property.


The [Input](../a-z/input.md) property is a character vector
that specifies the name of an object which is to be associated with every cell
in the Grid, or a vector of names whose elements are mapped to individual cells
through the [CellTypes](../a-z/celltypes.md) property. These
objects may be of type [Button](../a-z/button.md), [ColorButton](../a-z/colorbutton.md),
[Combo](../a-z/combo.md), [Edit](../a-z/edit.md), [Label](../a-z/label.md),
[Spinner](../a-z/spinner.md) or [TrackBar](../a-z/trackbar.md).
In addition, the [Input](../a-z/input.md) property may specify
instances of [OCXClass](../a-z/ocxclass.md) objects (ActiveX
controls) and [NetType](../a-z/nettype.md) objects (.NET classes).


If the [Input](../a-z/input.md) property is empty (the
default) the user may browse the data in the spreadsheet but may not alter it.
Furthermore, no feedback is provided as to which is the current cell. If the [Input](../a-z/input.md) property specifies the name of an object that is the child of the Grid itself,
this object *floats* from cell to cell as the user moves around the
spreadsheet, and the current cell is identified by its presence.


If the [Input](../a-z/input.md) property specifies the name of an external object (that is, an object that is *not* a child of the Grid), the contents of the current cell are copied into that
object as the user moves around the spreadsheet. In addition, the current cell
is identified by a thick border. In either case, the associated object is used
to impose formatting and validation.


If the [Input](../a-z/input.md) property specifies the name
of a [Label](../a-z/label.md) object, that object is used to
impose formatting, but the data is protected and may not be changed. If the [Label](../a-z/label.md) is a child of the Grid, it moves from cell to cell, and its characteristics ([Border](../a-z/border.md),
[FCol](../a-z/fcol.md), [BCol](../a-z/bcol.md) and [FontObj](../a-z/fontobj.md)) can be used to identify the
current cell. If the [Label](../a-z/label.md) is an external one,
no visual feedback is provided; even though the current cell (reflected by the [CurCell](../a-z/curcell.md) property) changes as the user moves around the Grid.


If the Input property specifies one or more instances of OCXClass objects
(ActiveX controls) and [NetType](../a-z/nettype.md) objects (.NET
classes), the [InputProperties](../a-z/inputproperties.md) property is used to map the [Values](../a-z/values.md) property
of the Grid to specific properties of the external object.


The [CellTypes](../a-z/celltypes.md) property is either an
empty numeric matrix (the default) or an integer matrix of the same shape as [Values](../a-z/values.md).
If specified, each element of [CellTypes](../a-z/celltypes.md) determines the index into various properties, including the [FCol](../a-z/fcol.md),
[BCol](../a-z/bcol.md), [CellFonts](../a-z/cellfonts.md) and [Input](../a-z/input.md) properties, to be used for the
corresponding cell. For example, if an element in [CellTypes](../a-z/celltypes.md) is 3, the 3rd element of [FCol](../a-z/fcol.md) is used for the
foreground colour of the corresponding cell, the 3rd element of [BCol](../a-z/bcol.md) specifies the background colour, and so forth.


The [CurCell](../a-z/curcell.md) property may be used to set
or query the current cell. The current cell is the cell which the user has
picked by clicking the mouse over it or by using the cursor keys. [CurCell](../a-z/curcell.md) is a 2-element vector containing the current cell's row number and column
number respectively and is `⎕IO` dependent. The [Index](../a-z/index.md) property specifies the
row and column number of the cell in the top-left corner of the Grid. It too is `⎕IO` dependent.


The [AutoExpand](../a-z/autoexpand.md) property is a
2-element Boolean vector which specifies whether (1) or not (0) new rows and
columns are added when the user presses the corresponding cursor key when at the
end of the block of cells. Its default value is (0 0).


The Grid object reports a [CellDown](../a-z/celldown.md) event
when the user depresses a mouse button over a cell. The event message contains
the row and column address of the cell in question which is `⎕IO` dependent. It also reports a similar [CellUp](../a-z/cellup.md) event when the mouse button is released and a [CellDblClick](../a-z/celldblclick.md) event when it is double-clicked. The number of the mouse button and the state of
the shift keys are also reported.


When the user moves to another cell, the Grid object reports a [CellMove](../a-z/cellmove.md) event. This simply reports the address of the new cell and may be used to take
some appropriate action when a particular cell is picked. If the user alters the
data in a cell and then attempts to move to another, the Grid reports a [CellChange](../a-z/cellchange.md) event. This can be used to perform validation.


Alternatively, the Grid may
report a [CellChanged](../a-z/cellchanged.md) event which occurs
after the [Values](../a-z/values.md) property has been updated
with the new cell contents. This may be used to perform immediate recalculation.


The [AddRow](../a-z/addrow.md) event is generated if the current
cell is in the last row of the Grid and the user presses Cursor Down. By
default, this operation adds a new row to the Grid, but you can attach a
callback to the [AddRow](../a-z/addrow.md) and selectively disable
this default action if required. The [AddCol](../a-z/addcol.md) event works in a similar manner for columns. Although the user has no direct
means of *inserting* a row or column, your application can do this by
calling [AddRow](../a-z/addrow.md) or [AddCol](../a-z/addcol.md) as a method on the Grid object. Typically this would be done in response to the
user selecting a [MenuItem](../a-z/menuitem.md) or pressing a [Button](../a-z/button.md).


The [ColChange](../a-z/colchange.md), [RowChange](../a-z/rowchange.md),
[DelRow](../a-z/delrow.md), [DelCol](../a-z/delcol.md) and [Undo](../a-z/undo.md) methods allow your application to
perform these corresponding operations.


The Grid object maintains a buffer of the most recent 8 changes made by the
user since the [Values](../a-z/values.md) property was last set
by [`⎕WC`](../../Language/System Functions/wc.htm) or [`⎕WS`](../../Language/System Functions/ws.htm).
Your application can restore these changes one by one by calling the [Undo](../a-z/undo.md) method. The [Undo](../a-z/undo.md) method restores the most recent
change made by the user and removes that change from the undo stack. It is
therefore not possible to "undo an undo".


The Grid supports the selection of a block or blocks of cells using the mouse
and/or the keyboard. The ability to select a range of cells is determined by the
[CellSelect](../a-z/cellselect.md) property. When the user
performs a selection, the Grid generates a [GridSelect](../a-z/gridselect.md) event. The range of cells currently selected is given by the [SelItems](../a-z/selitems.md) property.


If a block of cells has been selected, the user may delete the contents, and
cut or copy the contents of the cells to the clipboard by pressing Delete,
Shift+Delete or Ctrl+Insert respectively. These operations also generate [GridDelete](../a-z/griddelete.md),
[GridCut](../a-z/gridcut.md) and [GridCopy](../a-z/gridcopy.md) events which you can selectively disable using a callback function. You can
also perform these operations under program control by calling them as methods.


If more than one block of cells has been selected, these operations are
honoured only if the blocks begin and end on the same rows or begin and end on
the same columns. If so, the data placed in the clipboard is the result of
joining the blocks horizontally or vertically as appropriate.


The user may paste data from the clipboard into a Grid by pressing
Shift+Insert. Data is pasted into the currently selected block of cells, or, if
there is no selection, data is pasted starting at the current cell (`CurCell`).
The operation also generates a [GridPaste](../a-z/gridpaste.md) event, and, if the operation cannot proceed, a [GridPasteError](../a-z/gridpasteerror.md) event.


If you move the mouse pointer over any of the four edges of a selected block
of cells, the cursor changes to an arrow. You may now click and drag the border
of the selected cells with the mouse.


If you press the Ctrl key at the same
time, the contents of the selected cells are *copied* to the new location,
replacing the values in the block of cells onto which they are dropped.
Otherwise, the operation is treated as a *move* and the original block of
cells is emptied. This operation also generates a [GridDropSel](../a-z/griddropsel.md) event. You may only move or copy a *single* block of cells in this way.


The user may be permitted to resize the rows and/or columns of a Grid. This
is controlled by the [ResizeRows](../a-z/resizerows.md) and [ResizeCols](../a-z/resizecols.md) properties whose default values are 0. To allow the user to resize, set either
or both to 1. You can also specify a Boolean vector to allow specific
rows/columns to be resized while others are fixed. Two additional properties
named [ResizeRowTitles](../a-z/resizerowtitles.md) and [ResizeColTitles](../a-z/resizecoltitles.md) determine whether or not the user may alter the width of the row titles and the
height of the column titles.


If resizable, the cursor changes to a double-heads arrow when the user moves
the mouse pointer over the lines between the row and/or column titles. The user
may click and drag with the mouse to the desired size. The user may also
double-click. This causes the row or column to be resized to fit the data. Both
operations generate a [SetColSize](../a-z/setcolsize.md), or [SetRowSize](../a-z/setrowsize.md) event.


When you edit data in a Grid, the editing behaviour and the action of the
cursor movement keys is determined by the [InputMode](../a-z/inputmode.md) and [InputModeKey](../a-z/inputmodekey.md) properties.


The [GridFCol](../a-z/gridfcol.md) property specifies the
colour of all the grid lines. Alternatively, the [GridLineFCol](../a-z/gridlinefcol.md),
[GridLineWidth](../a-z/gridlinewidth.md), [RowLineTypes](../a-z/rowlinetypes.md) and [ColLineTypes](../a-z/collinetypes.md) properties may
specify the appearance for individual grid lines.


The [GridBCol](../a-z/gridbcol.md) property specifies the
colour used to fill the area between the end of the last column of data and the
right edge of the Grid and between the bottom row of data and the bottom edge of
the Grid.


The [RowTitleFCol](../a-z/rowtitlefcol.md) and [ColTitleFCol](../a-z/coltitlefcol.md) properties specify the colours to be used for the row and column titles
respectively.


The [ClipCells](../a-z/clipcells.md) property determines
whether or not the Grid displays partial cells. The default is 1. If you set [ClipCells](../a-z/clipcells.md) to 0, the Grid displays only complete cells and automatically fills the space
between the last visible cell and the edge of the Grid with the [GridBCol](../a-z/gridbcol.md) colour.


The [CellSet](../a-z/cellset.md) property is a Boolean array
that marks which cells are *set* (i.e. have values) and which are empty.
This allows you to edit large numeric matrices which contain empty cells without
a severe workspace penalty.


The [HScroll](../a-z/hscroll.md) and [VScroll](../a-z/vscroll.md) properties specify whether or not horizontal and vertical scrollbars are
displayed. Either property may be given the value `¯3` which forces the
corresponding scrollbar to appear always. [VScroll](../a-z/vscroll.md) and [HScroll](../a-z/hscroll.md) may only be set when the object is created and may not subsequently be changed.


The Grid object supports *comments* in a manner that is consistent with
the way that comments are handled by Microsoft Excel. If a comment is
associated with a cell, a small red triangle is displayed in its top right
corner. When the user rests the mouse pointer over a commented cell, the comment
is displayed as a pop-up with an arrow pointing back to the cell to which it
refers. The comment disappears when the mouse pointer is moved away. This is
referred to as *tip* behaviour. Comments may also be associated with row
and column titles.


Grid comments are managed by a set of methods, namely [AddComment](../a-z/addcomment.md),
[DelComment](../a-z/delcomment.md), [GetComment](../a-z/getcomment.md),
[ShowComment](../a-z/showcomment.md), [HideComment](../a-z/hidecomment.md) and [ClickComment](../a-z/clickcomment.md).


You may lock individual rows and columns using the [LockRows](../a-z/lockrows.md) and [LockColumns](../a-z/lockcolumns.md) methods. This facility is
however not supported in combination with hierarchical rows and/or columns which
are specified by [RowTitleDepth](../a-z/rowtitledepth.md) and [ColTitleDepth](../a-z/coltitledepth.md).


The Grid can display a *TreeView like* interface on the Row titles. In
this mode, the Grid automatically shows and hides row of data as the end user
expands and contracts nodes of the tree.


The [RowTreeDepth](../a-z/rowtreedepth.md) property is used
to specify the depth of rows in the Grid.


The appearance of the tree is determined by the [RowTreeStyle](../a-z/rowtreestyle.md) property.


User defined bitmaps can be used instead of the default Images by setting the
[RowTreeImages](../a-z/rowtreeimages.md) property.


The Grid generates [Expanding](../a-z/expanding.md) and [Retracting](../a-z/retracting.md) events when the user interacts with the tree.


The [RowSetVisibleDepth](../a-z/rowsetvisibledepth.md) method
can be used to set the visible depth of the tree.


