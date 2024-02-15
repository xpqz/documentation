




<h1 class="heading"><span class="name">Font</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | Loads a font resource |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Children | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Properties | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Methods | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Events | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |


Description


This object loads a Windows font into memory ready for use by another object.




The characteristics of the font are specified by its properties as follows :

| [PName](../a-z/pname.md) | A character vector containing the name of the font face.       The default is `'System'` . Note that       case is ignored when you specify the name, although it will be returned       correctly by `⎕WG` . |
| --- | ---  |
| [Size](../a-z/size.md) | An integer that specifies the character height of the font in pixels. |
| [Fixed](../a-z/fixed.md) | A Boolean value that specifies whether the font is fixed-width (1) or       proportional (0). |
| [Italic](../a-z/italic.md) | A Boolean value that specifies whether the font is italicised (1) or not       (0). |
| [Underline](../a-z/underline.md) | A Boolean value that specifies whether the font is underlined (1) or not (0). |
| [Weight](../a-z/weight.md) | An integer in the range 0-1000 that specifies how bold or heavy the font is (1000 = most bold). |
| [Rotate](../a-z/rotate.md) | A numeric scalar that specifies the angle of rotation of the font in       radians. The angle is measure from the x-axis in a counter-clockwise       direction. |
| [CharSet](../a-z/charset.md) | An integer that specifies the character encoding. |



The [Coord](../a-z/coord.md) property may be set to  `'Pixel'`, `'ScaledPixel'` or `'RealPixel'` when the object is created, but [Coord](../a-z/coord.md) may not subsequently be changed.


If you are using `'ScaledPixel'`, this means that your fonts will also be scaled up automatically, as well as the sizes of the controls in which they are used.


When you ask Windows to allocate a font, you may specify as many or as few of these properties as you wish. Windows actually supplies the font that most closely matches the attributes you have specified. The matching rules it uses are complex, and may be found in the appropriate Windows documentation.


The values of the above properties after `⎕WC` or `⎕WS` reflect the attributes of the font which has been allocated by Windows, and not necessarily the values you have specified. Furthermore, it is possible that changing the value of one property will cause the values of others to be changed.


If Coord is `'Pixel'`, it is interpreted as either `'RealPixel'` or `'ScaledPixel'` according to the value of the Dyalog_Pixel_Type parameter, which is either ScaledPixel or RealPixel. See 
Installation & Configuration Guide: 

Dyalog_Pixel_Type parameterDyalog_Pixel_Type on page 1.


If this parameter is not specified, the default is RealPixel. So by default, when you set Coord to Pixel, it will be treated as RealPixel.


