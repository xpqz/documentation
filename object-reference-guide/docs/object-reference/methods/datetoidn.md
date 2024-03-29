




<h1 class="heading"><span class="name">DateToIDN</span></h1>

Applies To: [Calendar](../a-z/calendar.md) [DateTimePicker](../a-z/datetimepicker.md) [Root](../a-z/root.md)


**Description**


This method is used to convert a date from `⎕TS` format into an [IDN](../Miscellaneous/International Day Number.htm) suitable for use in a [Calendar](../a-z/calendar.md) object.


The argument to DateToIDN is a 3-element array as follows:


| `[1]` | Year | Integer |
| --- | --- | ---  |
| `[2]` | Month | Integer |
| `[3]` | Day | Integer |


DateToIDN will also accept a single enclosed argument containing these values. In either case, if you specify more than 3 numbers, excess elements they will be ignored.

#### Examples
```apl
      F.C.DateToIDN 1998 9 11
36048
      F.C.DateToIDN ⊂1998 9 11
36048
      F.C.DateToIDN ⎕TS
36048
      F.C.DateToIDN,⎕TS
36048
```



