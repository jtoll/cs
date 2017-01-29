# SSH Remote Terminal Size

When using [`ssh`](https://en.wikipedia.org/wiki/Secure_Shell), if the column width is too narrow, change the width of the remote terminal console with `stty`.

```
stty cols 80
stty rows 24
```

From the `stty` man page:
```
cols number     Same as columns.
columns number  The terminal size is recorded as having number columns.
rows number     The terminal size is recorded as having number rows.
size		    The size of the terminal is printed as two numbers on a single line, first rows, then columns.
```
