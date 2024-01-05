# Vim from scratch

## Motivation
1. Learn vim 
2. Use raw config to use vim

## Website
[Learn VIM](https://learnvim.irian.to/)

## Starting Vim
```shell
vim 
```

### Quit
type `ZZ` or in vim type `:q`

### buffers
A buffer is an in-memory space where you can write and edit some text.
`:bn` `:bnext`, go to the next buffer
`:buffer` + file name. Vim can autocomplete with \<TAB\>
`:buffer + n`. go to the number `n` buffer.
`Ctrl-^`. go to previously buffer.
`bdelete` delete a buffer.

### Windows
A window is a viewport on a buffer. 

`:split` or `:sp`, split a window. And at the same time , you can append a file name
`:vsplit` or `:vs` virtical split a window.

Ctrl-W V    Opens a new vertical split
Ctrl-W S    Opens a new horizontal split
Ctrl-W C    Closes a window
Ctrl-W O    Makes the current window the only one on screen and closes other windows

:vsplit filename    Split window vertically
:split filename     Split window horizontally
:new filename       Create new window


### Tabs
A tab is a collection of window.
When you close a tab, You are just closing the layout of windows.

:tabnew file.txt    Open file.txt in a new tab
:tabclose           Close the current tab
:tabnext            Go to next tab
:tabprevious        Go to previous tab
:tablast            Go to last tab
:tabfirst           Go to first tab
`gt` to go to next tab page
`gT` to go to previous page

To start Vim with multiple tabs, you can do this from the terminal:
```bash
vim -p file1.js file2.js file3.js
```


### Vim Grammar
`verb` + `noun`

#### Nouns(Motions)
h    Left
j    Down
k    Up
l    Right
w    Move forward to the beginning of the next word
}    Jump to the next paragraph
$    Go to the end of the line

#### Verbs
y    Yank text (copy)
d    Delete text and save to register
c    Delete text, save to register, and start insert mode

#### More Nouns (Text Objects)

i + object    Inner text object
a + object    Outer text object

w         A word
p         A paragraph
s         A sentence
( or )    A pair of ( )
{ or }    A pair of { }
[ or ]    A pair of [ ]
< or >    A pair of < >
t         XML tags
"         A pair of " "
'         A Pair of ' '
`         A pair of ` `

#### Moving
##### Character
h   Left
j   Down
k   Up
l   Right


#### Word
w     Move forward to the beginning of the next word
W     Move forward to the beginning of the next WORD
e     Move forward one word to the end of the next word
E     Move forward one word to the end of the next WORD
b     Move backward to beginning of the previous word
B     Move backward to beginning of the previous WORD
ge    Move backward to end of the previous word
gE    Move backward to end of the previous WORD

##### Current line
0     Go to the first character in the current line
^     Go to the first nonblank char in the current line
g_    Go to the last non-blank char in the current line
$     Go to the last char in the current line
n|    Go the column n in the current line

##### follow and till
f    Search forward for a match in the same line
F    Search backward for a match in the same line
t    Search forward for a match in the same line, stopping before match
T    Search backward for a match in the same line, stopping before match
;    Repeat the last search in the same line using the same direction
,    Repeat the last search in the same line using the opposite direction

Sentence And Pargraph Navigation
(    Jump to the previous sentence
)    Jump to the next sentence

{    Jump to the previous paragraph
}    Jump to the next paragraph

Match 
%    Navigate to another match, usually works for (), [], {}

Line Number Navigation
gg    Go to the first line
G     Go to the last line
nG    Go to line n
n%    Go to n% in file

Window Navigation
H     Go to top of screen
M     Go to medium screen
L     Go to bottom of screen
nH    Go n line from top
nL    Go n line from bottom

Scrolling
Ctrl-E    Scroll down a line
Ctrl-D    Scroll down half screen
Ctrl-F    Scroll down whole screen
Ctrl-Y    Scroll up a line
Ctrl-U    Scroll up half screen
Ctrl-B    Scroll up whole screen


zt    Bring the current line near the top of your screen
zz    Bring the current line to the middle of your screen
zb    Bring the current line near the bottom of your screen

\*     Search for whole word under cursor forward
\#     Search for whole word under cursor backward
g*    Search for word under cursor forward
g#    Search for word under cursor backward

ma    Mark position with mark "a"
`a    Jump to line and column "a"
'a    Jump to line "a"

''    Jump back to the last line in current buffer before jump
``    Jump back to the last position in current buffer before jump
`[    Jump to beginning of previously changed / yanked text
`]    Jump to the ending of previously changed / yanked text
`<    Jump to the beginning of last visual selection
`>    Jump to the ending of last visual selection
`0    Jump back to the last edited file when exiting vim

''    Jump back to the last line in current buffer before jump
``    Jump back to the last position in current buffer before jump
`[    Jump to beginning of previously changed / yanked text
`]    Jump to the ending of previously changed / yanked text
`<    Jump to the beginning of last visual selection
`>    Jump to the ending of last visual selection
`-1    Jump back to the last edited file when exiting vim


'       Go to the marked line
`       Go to the marked position
G       Go to the line
/       Search forward
?       Search backward
n       Repeat the last search, same direction
N       Repeat the last search, opposite direction
%       Find match
(       Go to the last sentence
)       Go to the next sentence
{       Go to the last paragraph
}       Go to the next paragraph
L       Go to the the last line of displayed window
M       Go to the middle line of displayed window
H       Go to the top line of displayed window
[[      Go to the previous section
]]      Go to the next section
:s      Substitute
:tag    Jump to tag definition
