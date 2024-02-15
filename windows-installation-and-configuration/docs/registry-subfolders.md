# Registry Sub-Folders

A large amount of configuration information is maintained in the Windows Registry in sub-folders of the main folder identified by inifile.

Many of these values are dynamic, for example the position of the various Session windows, is maintained in a Registry sub-folder so that their appearance is maintained from one invocation of APL to the next. These types of Registry values are considered to be internal and are therefore not described herein.

However, any Registry Value that is maintained via a configuration dialog box will be named and described in the documentation for that dialog box in Chapter 2.

### AutoComplete

This contains registry entries that describe your personal AutoComplete options. See " Auto Complete Tab" on page 1.

### Captions

This contains registry entries to customise the Captions used in the various windows of the Dyalog APL IDE. See Window Captions  on page 1.

### Colours

This contains entries that describe the colour schemes you have and your personal preferences. See "Colour Selection Dialog" on page 1.

### Editor

This contains certain entries for the Editor.

### Event Viewer

This contains entries that describe your settings for the Event Viewer. See 
UI Guide: 

The Event Viewer.

### Explorer

This contains entries that describe your settings for the Workspace Explorer. See 
UI Guide: 

The Workspace Explorer Tool.

### files

This contains the size of your recently used file list (see " General Tab" on page 1) and the list of your most recently loaded workspaces.

### KeyboardShortcuts/keys

This contains the definitions of your Keyboard Shortcuts (Unicode Edition only). See "Keyboard Shortcuts Tab" on page 1.

### KeyboardShortcuts/chars

This contains the Registry Keyboard mappings between keystrokes and APL characters (Unicode Edition only). See 
UI Guide: 

Registry KeyboardUnicode Edition and the Registry Keyboard on page 1.

### LanguageBar

This contains the definitions of the symbols, tips, and help for the symbols in the LanguageBar.

### Printing

This contains the entries for your Printer Setup options. See  "Print Configuration Dialog Box" on page 1.

### SALT

This contains entries for SALT. See "SALT" on page 1.

### Search

This contains dynamic entries for the Find Objects Tool. See 
UI Guide: 

Find Objects Tool.

### Threads

This contains entries to remember your preferences for Threads. See 
UI Guide: 

The Threads Menu.

### UnicodeIME

This contains entries for the Dyalog Unicode IME.

### ValueTips

This contains entries for your Value Tips preferences. See 
UI Guide: 

Value Tips.

### WindowRects

This contains entries to maintain the position of various Session tool windows so that they remain consistent between successive invocations of APL.

### Array Editor

The Array Editor stores its settings in the following registry sub-folder:
```apl
HKEY_CURRENT_USER\Software\DavidLiebtag.com\Array Editor\1.1\Options
```
