




<h1 class="heading"><span class="name">BtnPix</span></h1>

| Applies To: | [Button](./button.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) |
| --- | --- | --- | ---  |


**Description**


This property is used to customise the appearance of a [Button](./button.md), [Menu](./menu.md) or [MenuItem](./menuitem.md). It specifies the names of or refs to up to 3 [Bitmap](./bitmap.md) objects to be used to display the object under different circumstances. In general, BtnPix is a 3-element vector of character vectors or refs. However, if it defines a single [Bitmap](./bitmap.md), it may be a single ref, a simple character scalar or vector, or an enclosed character vector.


The first [Bitmap](./bitmap.md) is displayed when the object is shown in its normal state. For a [Button](./button.md), this is when its [State](State.htm) is 0. The second [Bitmap](./bitmap.md) is used for a [Menu](./menu.md) or [MenuItem](./menuitem.md), when the object is selected (highlighted), or for a [Button](./button.md) when its [State](State.htm) is 1. The third [Bitmap](./bitmap.md) is used when the object is disabled by having its [Active](active.md) property set to 0.


For a [Button](./button.md) with [Style ](style.md)`'Push'`, this means that when the user clicks the [Button](./button.md), its appearance switches from the first to the second [Bitmap](./bitmap.md), and then back again. To maintain the standard 3-D appearance, the [Bitmap](./bitmap.md)s should contain the correct shadow lines around their edges. For [Button](./button.md)s with [Style ](style.md)`'Radio'` or `'Check'`, the [Button](./button.md) will display one or other of the two [Bitmap](./bitmap.md)s according to its current [State](State.htm).


For example, to have a [Button](./button.md) that displays a "Tick" or a "Cross" according to its [State](State.htm):
```apl
      'YES' ⎕WC 'Bitmap' 'C:\WDYALOG\YES.BMP'
      'NO'  ⎕WC 'Bitmap' 'C:\WDYALOG\NO.BMP'
      'f1.r1' ⎕WC 'Button'('Style' 'Check')
                          ('BtnPix' 'YES' 'NO')
```



