# Locals Lines

**Locals Lines** are lines in a defined function or operator that serve only to define local names.

A Locals Line may appear anywhere between line [0] and the first executable statement in the function or operator. Locals lines may  be interspersed with blank lines and comments. A Locals Line is identified by starting with a semicolon, prefixed optionally by whitespace. It may contain a comment at the end.

A Locals Line must be of the form `;name;name;name` where name is any valid APL name or  localisable system variable. The names are localised on entry to the function exactly as if they were specified as locals on line `[0]`.

## Example
```apl
      ∇ r←foo y;a;b       ⍝ some locals
               ;c;d       ⍝ some more locals  
        (a b c d)←y
        r←a+b-c×d 
      ∇

```

The function `foo` shown above localises names `a`,`b`,`c` and `d` (the indentation on line `[1]` in this example is entirely optional)

Syntactical errors on Locals Lines are detected when the user attempts to fix the function using the Editor or  `⎕FX` and will causes the operation to fail.

The local names defined in Locals Lines are syntax-coloured as locals.

You may skip Locals Lines when Tracing by checking the option labelled**Skip Locals Lines when Tracing** on the **Trace/Edit** tab of the **Options/Configure Dialog**,

![configuration dialog trace edit tab skip locals](../img/configuration-dialog-trace-edit-tab-skip-locals.png)
