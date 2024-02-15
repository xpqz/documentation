




<h1 class="heading"><span class="name">HotSpot</span></h1>
| Applies To: | [Cursor](../a-z/cursor.md) |
| --- | ---  |

| Applies To: | [Cursor](../a-z/cursor.md) | [Cursor](../a-z/cursor.md) |  |  |
| --- | --- | ---  |
| [Cursor](../a-z/cursor.md) |  |  |


Description


This property specifies the point within a [Cursor](../a-z/cursor.md) object that registers the cursor's position over another object. The mouse position, which is reported by various events, is actually the position of the cursor's HotSpot over the object in question.


HotSpot is a 2-element numeric vector that specifies the y-position and x-position of the hotspot within the cursor. A value of (0 0) specifies the top-left corner of the cursor; (31 31) specifies the bottom right corner of the cursor. The default value of HotSpot is (15 15).



