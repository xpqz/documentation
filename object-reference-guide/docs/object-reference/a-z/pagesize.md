




<h1 class="heading"><span class="name">PageSize</span></h1>

| Applies To: | [Form](./form.md) | [Scroll](./scroll.md) | [SubForm](./subform.md) |
| --- | --- | --- | ---  |


**Description**


For a [Form](./form.md) and [SubForm](./subform.md), the PageSize property is a 2-element integer vector which specifies the size of the thumb in the vertical and horizontal scrollbars respectively.


For a [Scroll](./scroll.md) object it is a single integer.


If PageSize is 0 (the default) it specifies the default thumb. Otherwise, PageSize is expressed in proportion to the corresponding value of [Range](range.md). For example, if [Range](range.md) is 1000, setting PageSize to 100 will obtain a thumb which is approximately 10% of the height or length of the scrollbar.






