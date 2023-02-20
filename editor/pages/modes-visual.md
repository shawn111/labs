
First generate a file to work on with 100 lines:

```plain
for i in {1..100}; do echo "This is line $i" >> lines-file; done
```{{exec}}


```plain
vim lines-file
```{{exec}}


---------

press `ESC`{{}} and type `:set nu`  to show line number

---------

press `Crtl+v`{{}} then move the cursor to select what you want.


