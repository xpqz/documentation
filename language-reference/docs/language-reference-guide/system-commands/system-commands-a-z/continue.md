




<h1 class="heading"><span class="name">Save Continuation</span><span class="command">)CONTINUE</span></h1>

This command saves the active workspace in the current working directory and ends the Dyalog APL session. The name of the workspace file is CONTINUE in upper-case with the extension defined by the [WSEXT parameter](../../UserGuide/Installation%20and%20Configuration/Configuration%20Parameters.htm#WSEXT).


Note that the values of all system variables (including `⎕SM`) and GUI objects are also saved in `CONTINUE`.


When a `CONTINUE` workspace is loaded, the latent expression (if any) is NOT executed.



