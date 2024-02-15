




<h1 class="heading"><span class="name">Cue</span></h1>

| Applies To: | [ButtonEdit](../a-z/buttonedit.md) | [Edit](../a-z/edit.md) |
| --- | --- | ---  |


**Description**


This  property specifies optional text to be displayed when a [ButtonEdit](../a-z/buttonedit.md) or an [Edit](../a-z/edit.md) object is empty. For an [Edit](../a-z/edit.md) object it applies only if the Style of the [Edit](../a-z/edit.md) object is `'Single'`.


The  Boolean property [ShowCueWhenFocused](../a-z/showcuewhenfocused.md)  determines whether or not the cue should also be displayed once the user has tabbed into or clicked on the input field (and thus given it the focus).

#### Example
```apl

      'F' ⎕WC 'Form' 'Cue Property'
      'F.E' ⎕WC 'Edit'
       F.E.Cue←'Enter Password'
```


![cue property](../img/cue-property.png)



**Note that this feature only applies if Native Look and Feel (see page 1) is enabled.**


**Note that this feature only applies if Native Look and Feel (see page 1) is enabled.**


