




<h1 class="heading"><span class="name">ValidIfEmpty</span></h1>

Applies To: [ButtonEdit](../a-z/buttonedit.md) [Edit](../a-z/edit.md) [Spinner](../a-z/spinner.md)


**Description**


This property applies to an [Edit](../a-z/edit.md) object with [Style](../a-z/style.md) Single and specifies whether or not an empty field is considered to be valid. It also applies to a [Spinner](../a-z/spinner.md). Its value is either 0 (an empty field is not valid) or 1 (an empty field is valid. If the [FieldType](../a-z/fieldtype.md) is Numeric, LongNumeric, Currency, Date or Time, the default value for ValidIfEmpty is 0. Otherwise, its default value is 1.


If ValidIfEmpty is 0 and the user attempts to *leave* the [Edit](../a-z/edit.md) object by shifting the input focus to another control, or by selecting a [Button](../a-z/button.md) or [MenuItem](../a-z/menuitem.md), the [Edit](../a-z/edit.md) object will generate a [BadValue](../a-z/badvalue.md) event. The [Text](../a-z/text.md) property will reflect the appearance of the field and be empty, but the [Value](../a-z/value.md) property will not be changed.


If ValidIfEmpty is 1 and the [FieldType](../a-z/fieldtype.md) is Numeric, LongNumeric, Currency, date or Time, the [Value](../a-z/value.md) property will be set to `⍬` when the user clears the field and leaves it.



