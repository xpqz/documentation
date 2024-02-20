




<h1 class="heading"><span class="name">I-Beam</span><span class="command">R←{X}(A⌶)Y</span></h1>

I-Beam is a monadic operator that provides a range of system related services.


**WARNING:** Although documentation is provided for I-Beam functions, any service provided using I-Beam should be considered as "experimental" and subject to change – without notice - from one release to the next. Any use of I-Beams in applications should therefore be carefully isolated in cover-functions that can be adjusted if necessary. See also: [RIDE and Experimental Features-related I-Beams](a-z/supplementary-i-beam-functions.md).



`A` is an integer that specifies the type of operation to be performed  as shown in the table below. `Y` is an array that supplies further information about what is to be done.


`X` may or may not be required depending on `A`.


`R` is the result of the derived function.


When attempting to use  I-Beam with an unsupported operation value, `A`, one of three different error messages will be reported:

- Invalid I-Beam function selection
- I-Beam function xxx has been withdrawn
- I-Beam function xxx is not supported by this interpreter

This allows the user to distinguish between operation values that have never been used, those that have been used in earlier versions but are no longer included in the current version, and those
that are valid in other editions or on other platforms other than the current interpreter.



The column labelled **O/S** indicates if a function applies only on Windows (W), only on Windows .NET Framework, (WF), only under IBM AIX (AIX), or only on non-Windows (X) platforms.


| A | Derived Function | O/S |
| --- | --- | ---  |
| `8` | [Inverted Table Index-of](a-z/inverted-table-index-of.md) |  |
| `85` | [Execute Expression](a-z/execute-expression.md) |  |
| `127` | [Overwrite Free Pockets](a-z/overwrite-free-pockets.md) |  |
| `180` | [Canonical Representation](a-z/canonical-representation.md) |  |
| `181` | [Unsqueezed Type](a-z/unsqueezed-type.md) |  |
| `200` | [Syntax Colouring](a-z/syntax-colouring.md) |  |
| `201` | [Syntax Colour Tokens](../I Beam Functions/Syntax Colour Tokens.htm) |  |
| `219` | [Compress/Decompress Vector of Short Integers](a-z/compress-vector-of-short-integers.md) |  |
| `220` | [Serialise/Deserialise Array](a-z/serialise-array.md) |  |
| `400` | [Compiler Control](a-z/compiler-control.md) |  |
| `600` | [Trap Control](a-z/trap-control.md) |  |
| `739` | [Temporary Directory](../I Beam Functions/Temporary Directory.htm#Temporary_Directory) |  |
| `819` | [Case Convert](a-z/case-convert.md) |  |
| `900` | [Called Monadically](a-z/called-monadically.md) |  |
| `950` | [Loaded Libraries](a-z/loaded-libraries.md) |  |
| `1010` | [Set Shell Script Debug Options](../I Beam Functions/Set Shell Script Debug Options.htm) |  |
| `1111` | [Number of Threads](a-z/number-of-threads.md) |  |
| `1112` | [Parallel Execution Threshold](a-z/parallel-execution-threshold.md) |  |
| `1159` | [Update Function Time and User Stamp](a-z/update-function-timestamp.md) |  |
| `1200` | [Format Date-time](../I Beam Functions/Format Datetime.htm) |  |
| `1302` | [Set aplcore Parameters](../I Beam Functions/Set aplcore Parameters.htm) |  |
| `1500` | [Hash Array](a-z/hash-array.md) |  |
| `2000` | [Memory Manager Statistics](a-z/memory-manager-statistics.md) |  |
| `2002` | [Specify Workspace Available](a-z/specify-workspace-available.md) |  |
| `2007` | [Disable Global Triggers](../I Beam Functions/Disable Global Triggers.htm#Trigger_Control) |  |
| `2010` | [Update DataTable](a-z/update-datatable.md) | WF |
| `2011` | [Read DataTable](a-z/read-datatable.md) | WF |
| `2014` | [Remove Data Binding](a-z/remove-data-binding.md) | WF |
| `2015` | [Create Data Binding Source](a-z/create-data-binding-source.md) | WF |
| `2016` | [Create .NET Delegate](a-z/create-net-delegate.md) | WF |
| `2017` | [Identify .NET Type](a-z/identify-net-type.md) | WF |
| `2022` | [Flush Session Caption](a-z/flush-session-caption.md) | W |
| `2023` | [Close all Windows](a-z/close-all-windows.md) |  |
| `2035` | [Set Dyalog Pixel Type](a-z/set-dyalog-pixel-type.md) | W |
| `2041` | [Override COM Default Value](a-z/override-com-default-value.md) | W |
| `2100` | [Export to Memory](a-z/export-to-memory.md) | W |
| `2101` | [Close .NET AppDomain](a-z/close-net-appdomain.md) | WF |
| `2250` | [Verify .NET Interface](../I Beam Functions/Verify .NET Interface.htm) |  |
| `2400` | [Set Workspace Save Options](a-z/set-workspace-save-options.md) |  |
| `2401` | [Expose Root Properties](a-z/expose-root-properties.md) |  |
| `2501` | [Discard thread on exit](a-z/discard-thread-on-exit.md) | W |
| `2502` | [Discard parked threads](a-z/discard-parked-threads.md) | W |
| `2503` | [Mark Thread as Uninterruptible](a-z/mark-thread-as-uninterruptible.md) |  |
| `2520` | [Use Separate Thread For .NET](a-z/use-separate-thread-for-net.md) | WF |
| `2704` | [Continue Autosave](../I Beam Functions/Continue Autosave.htm#Continue_Autosave) |  |
| `3002` | [Disable Component Checksum Validation](a-z/disable-component-checksum-validation.md) |  |
| `3012` | [Enable Compression of Large Components](../I Beam Functions/Enable Compression of Large Components.htm#Enable_LZ4_Frames) |  |
| `3500` | [Send Text to RIDE-embedded Browser](a-z/send-text-to-ride-embedded-browser.md) |  |
| `3501` | [Connected to the RIDE](a-z/connected-to-the-ride.md) |  |
| `3502` | [Manage RIDE Connections](a-z/manage-ride-connections.md) |  |
| `4000` | [Fork New Task](a-z/fork-new-task.md) | AIX |
| `4001` | [Change User](a-z/change-user.md) | X |
| `4002` | [Reap Forked Tasks](a-z/reap-forked-tasks.md) | AIX |
| `4007` | [Signal Counts](a-z/signal-counts.md) | X |
| `5171` | [Discard Source Information](../I Beam Functions/Discard Source Information.htm#Discard_Source_Information) |  |
| `5172` | [Discard Source Code](../I Beam Functions/Discard Source Code.htm#Discard_Source_Code) |  |
| `5176` | [List Loaded Files](a-z/list-loaded-files.md) |  |
| `5177` | [List Loaded File Objects](a-z/list-loaded-file-objects.md) |  |
| `5178` | [Remove Loaded File Object Info](../I Beam Functions/Remove Loaded File Object Info.htm) |  |
| `5179` | [Loaded File Object Info](../I Beam Functions/Loaded File Object Info.htm) |  |
| `7162` | [JSON Translate Name](a-z/json-translate-name.md) |  |
| `8415` | [Singular Value Decomposition](a-z/singular-value-decomposition.md) |  |
| `8674` | [Externalise Array](a-z/externalise-array.md) |  |
| `9468` | [Hash Table Size](../I Beam Functions/Hash Table Size.htm#Hash_Table_Size) |  |
| `9469` | [Lookup Table Size](../I Beam Functions/Lookup Table Size.htm#Lookup_Table_Size) |  |
| `16808` | [Sample Probability Distribution](a-z/sample-probability-distribution.md) |  |
| `50100` | [Line Count](a-z/line-count.md) |  |



