# SSH Remote Terminal Size

When using [`ssh`](https://en.wikipedia.org/wiki/Secure_Shell), if the column width is too narrow, change the width of the terminal console with `stty`.

```
stty cols 80
stty rows 24
```

From the `stty` man page:
```
* cols N	tell the kernel that the terminal has N columns
* rows N	tell the kernel that the terminal has N rows
* size		print the number of rows and columns according to the kernel
```
