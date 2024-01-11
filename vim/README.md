# Learn vim from scratch

1. Books

    [Practical Vim](https://digtvbg.com/files/LINUX/Practical%20Vim%20-%20Drew%20Neil_1241.pdf)

## Chapter1: The vim way

1. Meet the Dot Command.

    `>>` , `<<` indent this line.
    `>G` indent to for the current line until the end of the file.
    `j.` will do `>G` again.

2. Don't repeat yourself

    Two for the price of One

    |Compound Command | Equivalent in longhand |
    | :---:| :---: |
    | C | c$ |
    | s | cl |
    | S | ^C |
    | I | ^i |
    | A | $a |
    | o | A<CR> |
    | O | ko | 

3. Take On step Back, Then Forward

    f{char}, s{word}<ESC>,
    ; to repeat fellow,
    . to do the change again.

4. Act, Repeat, Reverse

    | Intent | Act | Repeat | Reverse |
    | --- | --- | :---: | :--: |
    | Make a change | {edit } | . | u |
    | Scan line for next char | f{char}/T{char} |; | , |
    | Scan line for previous character | F{char}/T{char} |; |, |
    | Scan document for next match | /pattern<CR> | n | N |
    | Scan document for previous match | ?pattern<CR> | n | N |
    | Perform substitutin | :s/target/replacement | & | u |
    | Execute a sequence of chages | qx{changes}q | @x | u |

5. Find and Replace by Hand

	`/content` search the first content
	`*` search the second content
	`cw{edit}<Esc>` change the content to edit word.
	`n` do the search again
	`.` do the last edit again.

6. Meet the Dot Formula

    The Ideal: One kyestroke to Move, One Keystroke to Execute.
