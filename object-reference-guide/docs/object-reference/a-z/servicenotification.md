




<h1 class="heading"><span class="name">ServiceNotification</span></h1>

| Applies To: | [Root](./root.md) |
| --- | ---  |


**Description**


This event is generated in an APL service whenever the Windows Service Control Manager (SCM) requests a change of state. See 
Installation & Configuration Guide: 

APL Application as a ServiceAPL Application as a Service on page 1.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 4-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'ServiceNotification'` or 94 |
| `[3]` | Action | Integer. |
| `[4]` | State | 7-element integer vector |



For further details, see the on-line documentation for `SERVICE_STATE` and the function `HashDefine` in the sample workspace `aplservice`.


The state of a Windows service is determined by the user and the Windows Service Control Manager (SCM).


When the SCM requests a change of state, the APL interpreter responds by setting its state to the corresponding **pending** level (SERVICE_STOPPED_PENDING, SERVICE_RUNNING_PENDING or SERVICE_PAUSED_PENDING) and then generates a [ServiceNotification](./servicenotification.md) event.


It is the responsibility of the APL service to process this event, perform the appropriate application tasks, and then respond (to the SCM) by calling the [SetServiceState](./setservicestate.md) method to confirm that the service has reached the desired state.


