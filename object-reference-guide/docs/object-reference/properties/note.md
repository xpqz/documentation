




<h1 class="heading"><span class="name">Note</span></h1>

| Applies To: | [Button](../a-z/button.md) |
| --- | ---  |


**Description**


The Note property applies only to a [Button](../a-z/button.md) whose Style is `'CommandLink'`.


It is a character vector (by default empty) that specifies text to be displayed below the [Caption](../a-z/caption.md).

#### Example:
```apl
'F'⎕WC'Form' 'CommandLink Button'
'F.clb'⎕WC'Button' 'Visit Us'('Style' 'CommandLink')  
F.clb.Size←80 200
F.clb.Note←'www.dyalog.com'
 
```


![commandlink button2](../img/commandlink-button2.png)



