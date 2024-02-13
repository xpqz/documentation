




<h1 class="heading"><span class="name">NO PIPES</span><span class="command">72</span></h1>

This message applies to the UNIX environment ONLY.


This message is given when the limit on the number of pipes communicating between tasks is exceeded.  An installation-set quota is assigned for each task.  An associated task may require more than one pipe.  The message occurs on attempting to exceed the account's quota when either:

- An APL session is started
- A non-APL task is started by the system function `⎕SH`
- An external variable is used.

It is necessary to release pipes by terminating sufficient tasks before proceeding with the required activity.  In practice, the error is most likely to occur when using the system function `⎕SH`.

#### Examples
```apl
      'via' ⎕SH 'via'
NO PIPES
      'via' ⎕SH 'via'
      ^
 
      'EXT/ARRAY' ⎕XT 'EXVAR'
NO PIPES
      'EXT/ARRAY' ⎕XT 'EXVAR'
                  ^
```



