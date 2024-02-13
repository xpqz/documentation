




<h1 class="heading"><span class="name">File Numbers</span><span class="command">R←⎕FNUMS</span></h1>

The result is an integer vector of the *file tie number* of all tied files.  If no files are tied, the result is empty.  The elements of the result are in the order in which the files were tied.

#### Examples
```apl

      '/home/pete/SALESFILE' ⎕FSTIE 16

      '../budget/COSTFILE' ⎕FSTIE 2

      'PROFIT' ⎕FCREATE 5

      ⎕FNUMS
16 2 5

      ⎕FNUMS,⎕FNAMES
16 /home/pete/SALESFILE
 2 ../budget/COSTFILE
 5 PROFIT

      ⎕FUNTIE ⎕FNUMS
      ⍴⎕FNUMS
0
```



