# Namespace Script Example

The DiaryStuff example illustrates the manner in which classes may be defined and used in a Namespace script.

DiaryStuff defines two Classes named `Diary` and `DiaryEntry`.

`Diary` contains a (private) Field named `entries`, which is simply a vector of instances of `DiaryEntry`. These are 2-element vectors containing a .NET DateTime object and a description.

The `entries` Field is initialised to an empty vector of `DiaryEntry` instances which causes the invocation of the default constructor `DiaryEntry.Make0` when `Diary` is fixed. See "Empty Arrays of Instances: Why ?" on page 1 for further explanation.

The `entries` Field is referenced through the `Entry` Property, which is defined as the [Default Property](../class-members/properties/default-property.md). This allows individual entries to be referenced and changed using indexing on a `Diary` Instance.

Note that `DiaryEntry` is defined in the script first (before `Diary`) because it is referenced by the initialisation of the `Diaries.entries` Field

Create a new instance of `Diary`.
```apl
      D←⎕NEW DiaryStuff.Diary
```

Add a new entry "meeting with John at 09:00 on April 30th"
```apl
      D.Add(2006 4 30 9 0)'Meeting with John'
 30/04/2006 09:00:00  Meeting with John 
```

Add another diary entry "Dentist at 10:00 on April 30th".
```apl
      D.Add(2006 4 30 10 0)'Dentist'
 30/04/2006 10:00:00  Dentist 
```

One of the benefits of the Namespace Script is that Classes defined within it (which are typically *related*) may be used *independently*, so we can create a stand-alone instance of `DiaryEntry`; "Doctor at 11:00"...
```apl
  Doc←⎕NEW DiaryStuff.DiaryEntry((2006 4 30 11 0)'Doctor')
      Doc
 30/04/2006 11:00:00  Doctor 
```

... and then use it to replace the second Diary entry with indexing:
```apl
      D[2]←Doc
```

and just to confirm it is there...
```apl
      D[2]
 30/04/2006 11:00:00  Doctor 
```

What am I doing on the 30th?
```apl
      D.DoingOn 2006 4 30
  30/04/2006 09:00:00  Meeting with John    ...
  ... 30/04/2006 11:00:00  Doctor  
```

Remove the 11:00 appointment...
```apl
      D.Remove 2006 4 30 11 0
1
```

and the complete Diary is...
```apl
      ⌷D
  30/04/2006 09:00:00  Meeting with John  
```

```apl
:Namespace DiaryStuff
:Using System
    
    :Class DiaryEntry
        :Field Public When
        :Field Public What
        ∇ Make(ymdhm wot)
          :Access Public
          :Implements Constructor
          When What←(⎕NEW DateTime(6↑5↑ymdhm))wot
          ⎕DF⍕When What
        ∇
        ∇ Make0
          :Access Public
          :Implements Constructor
          When What←⎕NULL''
        ∇
    :EndClass ⍝ DiaryEntry
```

```apl
    :Class Diary
        :Field Private entries←0⍴⎕NEW DiaryEntry
        ∇ R←Add(ymdhm wot)
          :Access Public
          R←⎕NEW DiaryEntry(ymdhm wot)
          entries,←R
        ∇
        ∇ R←DoingOn ymd;X
          :Access Public
          X←,(↑entries.When.(Year Month Day))^.=3 1⍴3↑ymd
          R←X/entries
        ∇
        ∇ R←Remove ymdhm;X
          :Access Public
          :If R←∨/X←entries.When=⎕NEW DateTime(6↑5↑ymdhm)
              entries←(~X)/entries
          :EndIf
        ∇
        :Property Numbered Default Entry
            ∇ R←Shape
              R←⍴entries
            ∇
            ∇ R←Get arg
              R←arg.Indexers⊃entries
            ∇
            ∇ Set arg
              entries[arg.Indexers]←arg.NewValue
            ∇
        :EndProperty
    :EndClass ⍝ Diary
    
:EndNamespace
```
