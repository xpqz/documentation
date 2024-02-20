




<h1 class="heading"><span class="name">Circle</span></h1>

[Parents](../ParentLists/Circle.htm) [Children](../ChildLists/Circle.htm) [Properties](../PropLists/Circle.htm) [Methods](../MethodLists/Circle.htm) [Events](../EventLists/Circle.htm)


Purpose: A Graphical object to draw circles, arcs, and pie-slices.


**Description**


The [Points](../a-z/points.md) property contains the co-ordinates of the centre of the circle. The size of the circle is determined by the [Radius](../a-z/radius.md) property. This specifies the radius along the x-axis, the height is calculated so that the object is circular.



The [ RadiusMode](../a-z/radiusmode.md) property determines whether or not the circle is adjusted by a pixel, if required in order to appear perfectly
round and perfectly centred. The default value is 0 (no adjustment is made).


The [Start](../a-z/start.md) and/or [End](../a-z/end.md) properties are used to draw partial circles. They specify start and end angles respectively, measuring from the x-axis in a counter-clockwise direction and are expressed in radians. The type of arc is controlled by [ArcMode](../a-z/arcmode.md) as follows :

#### ArcMode Effect


| 0 | An arc is drawn from [Start](../a-z/start.md) to [End](../a-z/end.md) . |
| --- | ---  |
| 1 | An arc is drawn from [Start](../a-z/start.md) to [End](../a-z/end.md) . In addition, a single straight line is drawn from one end of the arc to the other, resulting in a segment. |
| 2 | An arc is drawn from [Start](../a-z/start.md) to [End](../a-z/end.md) . In addition, two lines are drawn from each end of the arc to the centre, resulting in a pie-slice |


.


[Points](../a-z/points.md), [Radius](../a-z/radius.md), [Start](../a-z/start.md) and [End](../a-z/end.md) can specify vectors so that several arcs, circles, pie slices, etc. can be drawn in one call (and with one name).


If [Start](../a-z/start.md) is specified, but not [End](../a-z/end.md), end angles default to `(¯1↓+\Start),○2`. If [End](../a-z/end.md) is specified, but not [Start](../a-z/start.md), start angles default to `0,¯1↓+\End`


This means that you can draw a pie-chart using either [Start](../a-z/start.md) or [End](../a-z/end.md) angles; you do not have to specify both.

#### Examples:


A circle whose centre is (50,50) and radius 20
```apl
      'g.p1' ⎕WC 'Circle' (50 50) 20
```


An arc
```apl
      'g.arc' ⎕WC 'Circle' (50 50) 20 ('Start' (○0.75))('End' (○1.25))
```


Complete pie
```apl
      Data←12 27 21 40
      ANGLES←0,¯1↓((○2)÷+/Data)×+\Data
      COLS←(255 0 0)(0 255 0)(255 255 0)(0 0 255)
      PATS←1 2 3 4
      'g.pie' ⎕WC 'Circle' (50 50) 20 ('Start' ANGLES)
                  ('ArcMode' 2) ('FCol' (⊂0 0 0))
                  ('FStyle' PATS) ('FillCol' COLS)
```


Same pie as above, but 2nd slice is exploded by changing its centre and 4th slice is shrunk by reducing its radius :
```apl
      CY←50 52 50 50  ⍝ y-coord of centres
      R←20 20 20 17.5 ⍝ radii
      'g.pie' ⎕WC 'Circle' (50 CY) R ('Start' ANGLES)
                  ('ArcMode' 1) ('FCol' (⊂0 0 0))
                  ('FStyle' PATS) ('FillCol' COLS)
```


