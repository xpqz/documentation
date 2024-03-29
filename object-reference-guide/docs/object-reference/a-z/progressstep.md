



<h1 class="heading"><span class="name">ProgressStep</span></h1>

Applies To: [ProgressBar](./progressbar.md)


**Description**


This method is used to increment the thumb in a [ProgressBar](./progressbar.md) object.


The ProgressStep method is niladic.


The ProgressStep method causes the [ProgressBar](./progressbar.md) to attempt to increment its thumb by the value of its [Step](./step.md) property, taking into account the settings of its [Limits](./limits.md) and [Wrap](./wrap.md) properties.


If the values of the [Thumb](./thumb.md), [Step](./step.md) and [Limits](./limits.md) properties are `THUMB`, `STEP` and `LIMITS` respectively, the new value of Thumb (and the corresponding position of the highlighted bar) is:


if Wrap is 0:
```apl
      LIMITS[2]⌊THUMB+STEP
```


if Wrap is 1:
```apl
      LIMITS[1]+(1+LIMITS[2]-LIMITS[1])|THUMB+STEP-LIMITS[1]
```


