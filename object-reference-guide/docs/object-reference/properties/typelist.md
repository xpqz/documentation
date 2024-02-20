




<h1 class="heading"><span class="name">TypeList</span></h1>

Applies To: [OCXClass](../a-z/ocxclass.md) [OLEClient](../a-z/oleclient.md)


**Description**


This property reports the names of all the special data types defined for a particular COM object. It is a vector of character vectors returned by `⎕WG`. It may not be set using `⎕WC` or `⎕WS`. Further information about each data type 
may be obtained using [GetTypeInfo](../a-z/gettypeinfo.md).


Note that TypeList reports **all** of the data type names recorded in the .OCX file associated with the COM object. If several COM objects are provided within a single .OCX file, the entire set of data types reported may not necessarily be applicable to the Control in question.



