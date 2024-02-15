




<h1 class="heading"><span class="name">Thumb</span></h1>

Applies To

| Applies To: | [Form](./form.md) [ProgressBar](./progressbar.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [SubForm](./subform.md) [TrackBar](./trackbar.md) [UpDown](./updown.md) | [Form](./form.md) | [ProgressBar](./progressbar.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [SubForm](./subform.md) | [TrackBar](./trackbar.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [Form](./form.md) | [ProgressBar](./progressbar.md) | [Scroll](./scroll.md) |
| [Spinner](./spinner.md) | [SubForm](./subform.md) | [TrackBar](./trackbar.md) |
| [UpDown](./updown.md) |  |  |


Description


This property determines and reports the position of the *thumb* in an object.


For a [Scroll](./scroll.md) object, the value of Thumb is a single integer whose minimum value is 1 and whose maximum value is defined by the Range property.


For [ProgressBar](./progressbar.md), [Spinner](./spinner.md), [UpDown](./updown.md) and [TrackBar](./trackbar.md) objects, Thumb is a single numeric value in the range specified by the Limits property.


For a [Form](./form.md) or [SubForm](./subform.md) object, Thumb is a 2-element vector whose elements refer to the position of the thumb in the object's own built-in vertical and horizontal scrollbars respectively.


For other objects, Thumb is a single numeric value in the range defined by the Limits property.



