




<h1 class="heading"><span class="name">GetServiceState</span></h1>

| Applies To: | [Root](../a-z/root.md) |
| --- | ---  |


**Description**


This method is used to obtain the current state of a Dyalog APL service running under Windows. See  
Installation & Configuration Guide: 

APL Application as a ServiceAPL Application as a Service on page 1.


The GetServiceState method is niladic.


The result of the method is a 7-element numeric vector corresponding to the `SERVICE_STATUS` structure which is described in C++ as follows:
```apl
`typedef struct _SERVICE_STATUS {
  DWORD dwServiceType;
  DWORD dwCurrentState;
  DWORD dwControlsAccepted;
  DWORD dwWin32ExitCode;
  DWORD dwServiceSpecificExitCode;
  DWORD dwCheckPoint;
  DWORD dwWaitHint;
} SERVICE_STATUS, *LPSERVICE_STATUS;.`
```






For further details, see the on-line documentation for `SERVICE_STATE` and the function `HashDefine` in the sample workspace `aplservice`.


