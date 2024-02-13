




<h1 class="heading"><span class="name">Number of Threads</span><span class="command">R←1111⌶Y</span></h1>

Specifies how many threads are to be used for parallel execution.


If `Y` has the value `⍬`, `R` is the number of virtual processors in the machine.


Otherwise, `Y` is an integer that specifies the number of threads that are to be used henceforth for parallel execution. Prior to this call, the default number of threads is specified by the parameter  `APL_MAX_THREADS`. See 
Installation & Configuration Guide: 

APL_MAX_THREADS Parameter APL_MAX_THREADS on page 1.


Note that whatever the value of `Y`, Dyalog limits the number of threads to 64. So the effective number of threads is `Y⌊64`.



`R` is the previous value.


To set the number of threads to be the same as the number of virtual processors, execute the stamement:
```apl
      {}1111⌶ 1111⌶⍬
```


See 
Programming Reference Guide: 

 Parallel ExecutionParallel Execution
         on page 1 and Parallel Execution Threshold on page 1.


