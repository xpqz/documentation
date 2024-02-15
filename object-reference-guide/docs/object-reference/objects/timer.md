




<h1 class="heading"><span class="name">Timer</span></h1>
| Parents | Properties | Methods | Events |
| --- | --- | --- | ---  |

| Purpose: | To generate an action at regular intervals. |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| Properties | [Detach](../a-z/detach.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| Methods | [Detach](../a-z/detach.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| Events | [Detach](../a-z/detach.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [Wait](../a-z/wait.md) |  |


Description


The Timer object is used to generate an event at regular intervals. It can be
used to produce animation and to implement "repeaters" such as spin buttons.



The [Interval](../a-z/interval.md) property specifies how
often the Timer generates events and is defined in milliseconds. Its default
value is 1000.


The [Active](../a-z/active.md) property determines whether or
not the Timer generates events and can be used to switch the Timer off and on as
required.


The [FireOnce](../a-z/fireonce.md) property may be used to implement a once-off Timer event and has the value 0, 1 or 2.


Note that if you create a Timer object whose [Timer](../a-z/timer.md) event generates an error
(for example by attaching it to a non-existent callback) it may be very
difficult or even impossible to type into the Session, because the error will be
displayed over and over again. Care is therefore recommended.


