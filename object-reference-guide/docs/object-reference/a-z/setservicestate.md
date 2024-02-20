




<h1 class="heading"><span class="name">SetServiceState</span></h1>

Applies To: [Root](./root.md)


**Description**


This method is used to set the state of a Dyalog APL service running under Windows. See 
Installation & Configuration Guide: 

APL Application as a Service[APL Application as a Service](../../UserGuide/Installation and Configuration/APL Application as a Service.htm#A4S).


The argument to the SetServiceState method is the desired state of the service. This should be one of the following numeric values:


| SERVICE_STOPPED | 1 |
| --- | ---  |
| SERVICE_RUNNING | 4 |
| SERVICE_PAUSED | 7 |



The state of a Windows service is determined by the user and the Windows Service Control Manager (SCM).


When the SCM requests a change of state, the APL interpreter responds by setting its state to the corresponding **pending** level (SERVICE_STOPPED_PENDING, SERVICE_RUNNING_PENDING or SERVICE_PAUSED_PENDING) and then generates a [ServiceNotification](./servicenotification.md) event.


It is the responsibility of the APL service to process this event, perform the appropriate application tasks, and then respond (to the SCM) by calling the [SetServiceState](./setservicestate.md) method to confirm that the service has reached the desired state.


