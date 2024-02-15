




<h1 class="heading"><span class="name">Calendar</span></h1>

| [Parents](../ParentLists/Calendar.htm) | [Children](../ChildLists/Calendar.htm) | [Properties](../PropLists/Calendar.htm) | [Methods](../MethodLists/Calendar.htm) | [Events](../EventLists/Calendar.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The Calendar object provides an interface to the Month Calendar Control |
| --- | ---  |


**Description**


The Calendar object displays a calendar and allows the user to select a date or range of dates. The following illustration shows a default Calendar object.



![cal1](../img/cal1.gif)


The Calendar object will display as many full months as it can fit into the area specified by its Size property as shown below. The minimum size required to encompass a single month may be obtained using the [GetMinSize](../a-z/getminsize.md) method.
```apl
'F'⎕WC'Form' 'Example 2'('Size' 50 50)
'F.C'⎕WC'Calendar'('Size' 100 100)
```


![cal2](../img/cal2.gif)


The [Today](../a-z/today.md) property is an [IDN](../Miscellaneous/International%20Day%20Number.htm) that specifies the current day. Its default value is today's date, i.e. the local date set on your computer.


The [CircleToday](../a-z/circletoday.md) property is either 0 or 1 (the default) and specifies whether or not the Today date is circled when the Calendar object is showing the corresponding month.


The [HasToday](../a-z/hastoday.md) property is either 0 or 1 (the default) and specifies whether or not the Today date is displayed (using the Windows short date format) in the bottom left of the Calendar object.


The [WeekNumbers](../a-z/weeknumbers.md) property is either 0 (the default) or 1 and specifies whether or not the Calendar displays week numbers.


The following example shows a Calendar with both [CircleToday](../a-z/circletoday.md) and [HasToday](../a-z/hastoday.md) set to 0 and [WeekNumbers](../a-z/weeknumbers.md) set to 1.
```apl
'F'⎕WC'Form' 'Example 3'('Size' 30 30)
'F.C'⎕WC'Calendar'('CircleToday' 0)('HasToday' 0)('WeekNumbers' 1)
```


![cal3](../img/cal3.gif)


The [FirstDay](../a-z/firstday.md) property is an integer whose value is in the range 0-6. [FirstDay](../a-z/firstday.md) specifies the day that is considered to be the first day of the week and which appears first in the Calendar. The default value for [FirstDay](../a-z/firstday.md) depends upon your International Settings.


The [MinDate](../a-z/mindate.md) and [MaxDate](../a-z/maxdate.md) properties are integers that specify the minimum and maximum [IDN](../Miscellaneous/International%20Day%20Number.htm) values that the user may display and select in the Calendar object. By default these properties specify the entire range of dates that the Windows Month Calendar control can provide.


The [MonthDelta](../a-z/monthdelta.md) property specifies the number of months by which the Calendar object scrolls when the user clicks its scroll buttons. The default is empty (zilde) which implies the number of months currently shown.


The [Style](../a-z/style.md) property may be either `'Single'` (the default) or '`Multi'`. If [Style](../a-z/style.md) is `'Single'`, the user may select a single date. If [Style](../a-z/style.md) is '`Multi'`, the user may select a contiguous range of dates. In this case, the maximum number of contiguous days that can be selected is defined by the [MaxSelCount](../a-z/maxselcount.md) property which is an integer whose default value is 7.


The [SelDate](../a-z/seldate.md) property is a 2-element integer vector of [IDN](../Miscellaneous/International%20Day%20Number.htm) values that identifies the first and last dates that are currently selected.


When the user selects one or more dates, the Calendar object generates a [SelDateChange](../a-z/seldatechange.md) event. This event is also generated when the Calendar object is scrolled, and the selection changes automatically to another month.


The Calendar displays day numbers using either the normal or the bold font attribute and you may specify which attribute is to be used for each day shown. However, the Calendar object does not store this information beyond the month or months currently displayed.


When the Calendar control scrolls (and potentially at other times), it generates a [GetDayStates](../a-z/getdaystates.md) event that, in effect, asks you (the APL program) to tell it which (if any) of the dates that are about to be shown should be displayed in bold.


If you wish *any* dates to be displayed using the bold font attribute, you must attach a callback function to the [GetDayStates](../a-z/getdaystates.md) event which returns this information in its result. By default, all dates are displayed using the normal font attribute, so you only need a callback function if you want any dates to be displayed in bold.


You may also set the font attribute for particular days in the range currently displayed by calling [GetDayStates](../a-z/getdaystates.md) as a method.


The [CalendarCols](../a-z/calendarcols.md) property specifies the colours used for various elements in the Calendar object.


You may convert dates between [IDN](../Miscellaneous/International%20Day%20Number.htm) and `⎕TS` representations using the [IDNToDate](../a-z/idntodate.md) and [DateToIDN](../a-z/datetoidn.md) methods. Note that these methods apply to **all** objects and not just to the Calendar object itself.


The [GetVisibleRange](../a-z/getvisiblerange.md) method reports the range of dates that is currently visible in the Calendar object.


