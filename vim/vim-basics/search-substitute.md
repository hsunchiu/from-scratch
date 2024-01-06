## Smart Case Sensitivity
```vimrc
set ignorecase smartcase
```
`/\CHello` will only search `Hello`.
You can target the first "hello" with /^hello. The character that follows ^ must be the first character in a line. To target the last "hello", run /hello$. The character before $ must be the last character in a line.

```txt
hello vim
hola vim
salve vim
bonjour vim
```
