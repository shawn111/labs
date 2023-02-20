
- hx --health (c)

```
hx --health c
Configured language server: clangd
Binary for language server: Not found in $PATH
Configured debug adapter: lldb-vscode
Binary for debug adapter: Not found in $PATH
Highlight queries: ✓
Textobject queries: ✓
Indent queries: ✓
```

```
$ hx --health
Config file: default
Language file: default
Log file: /home/shawn111/.cache/helix/helix.log
Runtime directory: /nix/store/14r96fbcnqv4rcpwc964yirkr9hwnchk-helix-22.12/lib/runtime
Clipboard provider: termcode
System clipboard provider: termcode

Language      LSP           DAP           Highlight     Textobject    Indent        
astro         None          None          ✓             ✘             ✘             
awk           ✘ awk-lang…   None          ✓             ✓             ✘             
bash          ✘ bash-lan…   None          ✓             ✘             ✘               
```
