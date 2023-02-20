> prepare helix

```plain
mkdir -p $HOME/bin
curl -L https://github.com/helix-editor/helix/releases/download/22.12/helix-22.12-x86_64.AppImage -o $HOMEmbin/hx
chmod +x $HOME/bin/hx

export PATH=$HOME/bin:$PATH
```{{exec}}


```plain
git clone --depth=1 https://github.com/shawn111/labs
cd labs/hello-world 
```{{exec}}

```
vim hello.py
```

```
hx hello.py
```
:hsplit hello.go
:vsplit hello.rs


