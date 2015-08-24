`i` for the insert mode, and `ESC` back to the normal mode

`h` to the left, `j` goes down, `k` goes up and `l` goes right

`w` moves to the start of next word

`e` moves to the end of the word

`b` moves to the beginning of the word

number before above command works perfectly

`30i- ESC` will make an underline 30 times, `3igo ESC`will print gogogo for you

`f` to find next occurrence of a character, e.g. `fo`, `F` to find previous occurrence of a character

If in the text that is structured with parentheses or brackets, `(` or `[` or `{`, use `%` to jump to the matching parenthesis or bracket.

`0` to the beginning of a line, `$` to the end of the line.

`*` to find the next occurrence of the word under cursor, and the previous with `#`

`gg` takes you to the beginning of the file; `G` to the end

To jump directly to a specific line, give its `line number` along with `G`

`/` to find the text you are looking for, and use `n` or `N` to find the next or previous occurrences

`o` to insert text into a new line below and `O` to insert text to a new line above

`x` and `X` to delete the character under the cursor and to the left of the cursor, respectively

use `r` to replace only one character under your cursor, without changing to insert mode

`d` is the delete command, `dd` delete a line, `dw` deletes the first word on the right side of the cursor, and it also copies the content, os you can paste it with `p` to another location.

remove two words `d2e`

`.` to repeat the previous command

`visual mode`, use `v` to enter visual mode, in the visual mode, you select text using movement keys before you decide what to do with it.

`u` to undo and `ctrl+R` for redo
