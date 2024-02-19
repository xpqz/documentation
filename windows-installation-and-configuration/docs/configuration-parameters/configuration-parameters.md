# Configuration Parameters

### Introduction

Dyalog APL is customised using a set of [configuration parameters](#Configuration_Parameter_Table). These may be defined  in a number of ways, which take precedence as follows:

- Command-line settings
- Application configuration file settings
- Environment variable settings
- User configuration file settings
- Settings in the registry section defined by the IniFile parameter (Windows only)
- Built-in defaults

This scheme provides a great deal of flexibility, and a system whereby you can override one setting with another. For example, you can define your normal workspace size (*maxws*) in the Registry, but override it with a new value specified on the APL command line. The way this is done is described in the following section.

Furthermore, you are not limited to the set of parameters employed by APL itself as you may add parameters of your own choosing.

Although for clarity parameter names are given here in mixed case, they are case-independent under Windows. Under UNIX and Linux, if Dyalog parameters are specified as environment variables they must be named entirely in upper-case.

Note that the value of a parameter obtained by the GetEnvironment method (see GetEnvironment MethodGetEnvironment on page 1) uses exactly the same set of rules.

The following section details those parameters that are implemented by Registry Values in the top-level folder identified by **IniFile**. Values that are implemented in sub-folders are *mainly* internal and are not described in detail here. However, any Value that is maintained via a configuration dialog box will be named and described in the documentation for that dialog box in The APL Environment.

### Specifying Size-related Parameters

Several of the configuration parameters define sizes.

The value of the parameter must consist of an integer value, optionally followed immediately by a single character which denotes the units to be used. If the value contains no character the units are assumed to be KiB.

Valid values for units are:

K(KiB), M(MiB), G(GiB), T(TiB), P(PiB) and E(EiB).

Specifying an invalid value will prevent Dyalog APL from starting.

### Changing parameter values in the Registry

You can change parameters in the Registry in one of two ways:

- Using the Configuration dialog box that is obtained by selecting *Configure* from the *Options* menu on the Dyalog APL/W session. See "The Configuration Dialog Box" on page 1 for details.
- By directly editing the Windows Registry using `REGEDIT.EXE` or `REGEDIT32.EXE`. This is necessary for parameters that are not editable via the Configuration dialog box.

### Configuration Parameters

| [AddClassHeaders](a-z/addclassheaders.md) | [AplCoreName](a-z/aplcorename.md) | [APLK](a-z/aplk.md) | [APLKeys](a-z/aplkeys.md) | [APLNID](a-z/aplnid.md) |
| --- | --- | --- | --- | ---  |
| [APLT](a-z/aplt.md) | [APLTrans](a-z/apltrans.md) | [APL_CODE_E_MAGNITUDE](a-z/apl-code-e-magnitude.md) | [APL_COMPLEX_AS_V12](a-z/apl-complex-as-v12.md) | [APL_FAST_FCHK](a-z/apl-fast-fchk.md) |
| [APL_FCREATE_PROPS_C](a-z/apl-fcreate-props-c.md) | [APL_FCREATE_PROPS_J](a-z/apl-fcreate-props-j.md) | [APL_MAX_THREADS](a-z/apl-max-threads.md) | [APL_TextInAplCore](Configuration Parameters/APL_TextInAplCore.htm) | [AutoComplete/CancelKey1](Configuration Parameters/AutoComplete/CancelKey1.htm) |
| [AutoComplete/CancelKey2](Configuration Parameters/AutoComplete/CancelKey2.htm) | [AutoComplete/Cols](Configuration Parameters/AutoComplete/Cols.htm) | [AutoComplete/CommonKey1](Configuration Parameters/AutoComplete/CommonKey1.htm) | [AutoComplete/CompleteKey1](Configuration Parameters/AutoComplete/CompleteKey1.htm) | [AutoComplete/CompleteKey2](Configuration Parameters/AutoComplete/CompleteKey2.htm) |
| [AutoComplete/Enabled](Configuration Parameters/AutoComplete/Enabled.htm) | [AutoComplete/History](Configuration Parameters/AutoComplete/History.htm) | [AutoComplete/HistorySize](Configuration Parameters/AutoComplete/HistorySize.htm) | [AutoComplete/PrefixSize](Configuration Parameters/AutoComplete/PrefixSize.htm) | [AutoComplete/Rows](Configuration Parameters/AutoComplete/Rows.htm) |
| [AutoComplete/ShowFiles](a-z/autocomplete/showfiles.md) | [AutoDPI](a-z/autodpi.md) | [AutoFormat](a-z/autoformat.md) | [AutoIndent](a-z/autoindent.md) | [Auto_PW](a-z/auto-pw.md) |
| [CFEXT](a-z/cfext.md) | [ClassicMode](a-z/classicmode.md) | [ClassicModeSavePosition](a-z/classicmodesaveposition.md) | [CMD_PREFIX and CMD_POSTFIX](a-z/cmd-prefix-and-cmd-postfix.md) | [ConfigFile](Configuration Parameters/ConfigFile.htm) |
| [Confirm_Abort](a-z/confirm-abort.md) | [Confirm_Close](a-z/confirm-close.md) | [Confirm_Fix](a-z/confirm-fix.md) | [Confirm_Session_Delete](a-z/confirm-session-delete.md) | [Default_DIV](a-z/default-div.md) |
| [Default_IO](a-z/default-io.md) | [Default_ML](a-z/default-ml.md) | [Default_PP](a-z/default-pp.md) | [Default_PW](a-z/default-pw.md) | [Default_RTL](a-z/default-rtl.md) |
| [Default_WX](a-z/default-wx.md) | [DMXOutputOnError](a-z/dmxoutputonerror.md) | [DockableEditWindows](a-z/dockableeditwindows.md) | [DoubleClickEdit](a-z/doubleclickedit.md) | [Dyalog](a-z/dyalog.md) |
| [DyalogEmailAddress](a-z/dyalogemailaddress.md) | [DyalogHelpDir](a-z/dyaloghelpdir.md) | [DyalogInstallDir](a-z/dyaloginstalldir.md) | [DyalogLink](Configuration Parameters/DyalogLink.htm) | [DyalogStartup](Configuration Parameters/DyalogStartup.htm) |
| [DyalogStartupSE](Configuration Parameters/DyalogStartupSE.htm) | [DyalogStartup_X](Configuration Parameters/DyalogStartup_X.htm) | [DyalogWebSite](a-z/dyalogwebsite.md) | [DYALOG_DISCARD_FN_SOURCE](Configuration Parameters/DYALOG_DISCARD_FN_SOURCE.htm) | [DYALOG_EVENTLOGGINGLEVEL](a-z/dyalog-eventlogginglevel.md) |
| [DYALOG_EVENTLOGNAME](a-z/dyalog-eventlogname.md) | [DYALOG_GUTTER_ENABLE](Configuration Parameters/DYALOG_GUTTER_ENABLE.htm) | [Dyalog_LineEditor_Mode](Configuration Parameters/Dyalog_LineEditor_Mode.htm) | [Dyalog_NETCore](Configuration Parameters/Dyalog_NETCore.htm) | [DYALOG_NOPOPUPS](a-z/dyalog-nopopups.md) |
| [Dyalog_Pixel_Type](a-z/dyalog-pixel-type.md) | [DYALOG_SERIAL](a-z/dyalog-serial.md) | [EditorState](a-z/editorstate.md) | [Edit_Cols](Configuration Parameters/Edit_Cols.htm) | [Edit_First_X](Configuration Parameters/Edit_First_X.htm) |
| [Edit_First_Y](Configuration Parameters/Edit_First_Y.htm) | [Edit_Offset_X](Configuration Parameters/Edit_Offset_X.htm) | [Edit_Offset_Y](Configuration Parameters/Edit_Offset_Y.htm) | [Edit_Rows](Configuration Parameters/Edit_Rows.htm) | [ENABLE_CEF](a-z/enable-cef.md) |
| [ErrorOnExternalException](a-z/erroronexternalexception.md) | [ExternalHelpURL](a-z/externalhelpurl.md) | [File_Stack_Size](Configuration Parameters/File_Stack_Size.htm) | [Greet_Bitmap](a-z/greet-bitmap.md) | [History_Size](a-z/history-size.md) |
| [IniFile](a-z/inifile.md) | [InitFullScriptNormal](Configuration Parameters/InitFullScriptNormal.htm) | [InitFullScriptSusp](Configuration Parameters/InitFullScriptSusp.htm) | [InitialKeyboardLayout](a-z/initialkeyboardlayout.md) | [InitialKeyboardLayoutInUse](a-z/initialkeyboardlayoutinuse.md) |
| [InitialKeyboardLayoutShowAll](a-z/initialkeyboardlayoutshowall.md) | [Input_Size](a-z/input-size.md) | [KeyboardInputDelay](a-z/keyboardinputdelay.md) | [Load](Configuration Parameters/Load.htm) | [localdyalogdir](a-z/localdyalogdir.md) |
| [Log_File](a-z/log-file.md) | [Log_File_InUse](a-z/log-file-inuse.md) | [Log_Size](a-z/log-size.md) | [LX](Configuration Parameters/LX.htm) | [MapChars](a-z/mapchars.md) |
| [MaxAplCores](a-z/maxaplcores.md) | [MaxWS](a-z/maxws.md) | [OverstrikesPopup](a-z/overstrikespopup.md) | [PassExceptionsToOpSys](a-z/passexceptionstoopsys.md) | [PFKey_Size](a-z/pfkey-size.md) |
| [ProgramFolder](a-z/programfolder.md) | [PropertyExposeRoot](a-z/propertyexposeroot.md) | [PropertyExposeSE](a-z/propertyexposese.md) | [QCMD_Timeout](a-z/qcmd-timeout.md) | [ResolveOverstrikes](a-z/resolveoverstrikes.md) |
| [RIDE_Init](Configuration Parameters/RIDE_Init.htm) | [RIDE_Spawned](Configuration Parameters/RIDE_Spawned.htm) | [RunAsService](a-z/runasservice.md) | [SaveContinueOnExit](a-z/savecontinueonexit.md) | [SaveLogOnExit](a-z/savelogonexit.md) |
| [SaveSessionOnExit](a-z/savesessiononexit.md) | [Serial](a-z/serial.md) | [SessionOnTop](a-z/sessionontop.md) | [Session_File](a-z/session-file.md) | [ShowStatusOnError](a-z/showstatusonerror.md) |
| [SingleTrace](a-z/singletrace.md) | [SkipLines](Configuration Parameters/SkipLines.htm) | [SM_Cols](Configuration Parameters/SM_Cols.htm) | [SM_Rows](Configuration Parameters/SM_Rows.htm) | [StatusOnEdit](a-z/statusonedit.md) |
| [TabStops](a-z/tabstops.md) | [ToolBarsOnEdit](Configuration Parameters/ToolBarsOnEdit.htm) | [TraceStopMonitor](a-z/tracestopmonitor.md) | [Trace_First_X](Configuration Parameters/Trace_First_X.htm) | [Trace_First_Y](Configuration Parameters/Trace_First_Y.htm) |
| [Trace_Level_Warn](a-z/trace-level-warn.md) | [Trace_Offset_X](Configuration Parameters/Trace_Offset_X.htm) | [Trace_Offset_Y](Configuration Parameters/Trace_Offset_Y.htm) | [Trace_On_Error](Configuration Parameters/Trace_On_Error.htm) | [UCMDCacheFile](Configuration Parameters/UCMDCacheFile.htm) |
| [UnicodeToClipboard](a-z/unicodetoclipboard.md) | [URLHighlight](Configuration Parameters/URLHighlight.htm) | [UseExternalHelpURL](a-z/useexternalhelpurl.md) | [UserConfigFile](Configuration Parameters/UserConfigFile.htm) | [UseXCV](Configuration Parameters/UseXCV.htm) |
| [ValueTips/ColourScheme](Configuration Parameters/ValueTips/ColourScheme.htm) | [ValueTips/Delay](Configuration Parameters/ValueTips/Delay.htm) | [ValueTips/Enabled](a-z/valuetips/enabled.md) | [WantsSpecialKeys](a-z/wantsspecialkeys.md) | [WrapSearch](a-z/wrapsearch.md) |
| [WrapSearchMsgBox](a-z/wrapsearchmsgbox.md) | [WSEXT](a-z/wsext.md) | [WSPath](a-z/wspath.md) | [XPLookAndFeel](a-z/xplookandfeel.md) | [YY_Window](a-z/yy-window.md) |
