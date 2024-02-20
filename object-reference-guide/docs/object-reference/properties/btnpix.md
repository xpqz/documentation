




<h1 class="heading"><span class="name">BtnPix</span></h1>

Applies To: [Button](../a-z/button.md) [Menu](../a-z/menu.md) [MenuItem](../a-z/menuitem.md)


**Description**


This property is used to customise the appearance of a [Button](../a-z/button.md), [Menu](../a-z/menu.md) or [MenuItem](../a-z/menuitem.md). It specifies the names of or refs to up to 3 [Bitmap](../a-z/bitmap.md) objects to be used to display the object under different circumstances. In general, BtnPix is a 3-element vector of character vectors or refs. However, if it defines a single [Bitmap](../a-z/bitmap.md), it may be a single ref, a simple character scalar or vector, or an enclosed character vector.


The first [Bitmap](../a-z/bitmap.md) is displayed when the object is shown in its normal state. For a [Button](../a-z/button.md), this is when its [State](../a-z/state.md) is 0. The second [Bitmap](../a-z/bitmap.md) is used for a [Menu](../a-z/menu.md) or [MenuItem](../a-z/menuitem.md), when the object is selected (highlighted), or for a [Button](../a-z/button.md) when its [State](../a-z/state.md) is 1. The third [Bitmap](../a-z/bitmap.md) is used when the object is disabled by having its [Active](../a-z/active.md) property set to 0.


For a [Button](../a-z/button.md) with [Style ](../a-z/style.md)`'Push'`, this means that when the user clicks the [Button](../a-z/button.md), its appearance switches from the first to the second [Bitmap](../a-z/bitmap.md), and then back again. To maintain the standard 3-D appearance, the [Bitmap](../a-z/bitmap.md)s should contain the correct shadow lines around their edges. For [Button](../a-z/button.md)s with [Style ](../a-z/style.md)`'Radio'` or `'Check'`, the [Button](../a-z/button.md) will display one or other of the two [Bitmap](../a-z/bitmap.md)s according to its current [State](../a-z/state.md).


For example, to have a [Button](../a-z/button.md) that displays a "Tick" or a "Cross" according to its [State](../a-z/state.md):
```apl
      'YES' ⎕WC 'Bitmap' 'C:\WDYALOG\YES.BMP'
      'NO'  ⎕WC 'Bitmap' 'C:\WDYALOG\NO.BMP'
      'f1.r1' ⎕WC 'Button'('Style' 'Check')
                          ('BtnPix' 'YES' 'NO')
```



