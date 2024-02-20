




<h1 class="heading"><span class="name">ExportedVars</span></h1>

Applies To: [OLEServer](../a-z/oleserver.md)


**Description**


This property specifies the variables to be exposed as properties by an [OLEServer](../a-z/oleserver.md) object.


ExportedVars may be set to 0 (none), 1 (all), or a vector of character vectors containing the names of the variables to be exported.


Note that you may not export external variables or shared variables, or variables in other namespaces.


If you wish to export a new variable from your [OLEServer](../a-z/oleserver.md), and ExportedVars is not 1, you must explicitly reset the value of the ExportedVars property before you re-save the workspace.



