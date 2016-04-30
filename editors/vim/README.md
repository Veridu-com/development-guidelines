# Suggestions:
- Use the following for your .vimrc (this uses 4 spaces instead of tabs):

```vimrc
:set expandtab
:set tabstop=4
:set shiftwidth=4
:set nu
:set si

" auto go back to last pos:
if has("autocmd")
  au BufReadPost * if line("'\"") > 1 && line("'\"") <= line("$") | exe "normal! g'\"" | endif
endif
```

- To retab your document, transforming tabs into spaces issue the command `:retab`
