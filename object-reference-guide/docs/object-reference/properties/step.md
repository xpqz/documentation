



<h1 class="heading"><span class="name">Step</span></h1>

Applies To

| Applies To: | [Form](../a-z/form.md) [Locator](../a-z/locator.md) [ProgressBar](../a-z/progressbar.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [SubForm](../a-z/subform.md) [TrackBar](../a-z/trackbar.md) [UpDown](../a-z/updown.md) | [Form](../a-z/form.md) | [Locator](../a-z/locator.md) | [ProgressBar](../a-z/progressbar.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [SubForm](../a-z/subform.md) | [TrackBar](../a-z/trackbar.md) | [UpDown](../a-z/updown.md) |  |
| --- | --- | ---  |
| [Form](../a-z/form.md) | [Locator](../a-z/locator.md) | [ProgressBar](../a-z/progressbar.md) |
| [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [SubForm](../a-z/subform.md) |
| [TrackBar](../a-z/trackbar.md) | [UpDown](../a-z/updown.md) |  |


Description


This property determines the size of changes reported when the user clicks a scroll arrow (small change) or clicks on the body of the scrollbar (large change). The object's [Thumb](../a-z/thumb.md) property increases or decreases by this amount.


For a [Scroll](../a-z/scroll.md) object, Step is a 2-element numeric vector whose first element specifies the value of the "small change" and whose second element specifies the value of the "large change".


For a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), Step is a 4-element numeric vector. The first two elements refer to the [Form](../a-z/form.md)'s vertical scrollbar and the second two elements refer to the [Form](../a-z/form.md)'s horizontal scrollbar.


For the above objects, values of Step must be between 1 and the value of the [Range](../a-z/range.md) property.


For a [Locator](../a-z/locator.md) object, Step is a 2-element integer vector (default value 1 1) that specifies the increments (in pixels) by which the size or position of the [Locator](../a-z/locator.md) changes in the Y and X directions respectively as the user moves the [Locator](../a-z/locator.md).


