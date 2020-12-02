### VIM Shortcuts and Operations

> commands without `:` should be entered in a command mode (after pressing the "esc" key)
> The phrase 'current' represents the cursor's position

### ToC:
- [Typing/Inserting](#type)
- [Delete/Replace](#del)
- [Undo/Redo](#do)
- [Cut, Copy, Paste](#edit)
- [Navigation](#nav)
- [Line Actions](#line)
- [Word Actions](#word)
- [Search Operations](#search)
- [Replace Operations](#replace)
- [File Operataions](#file)

#### Typing: <a name="type"></a>
```bash
# start typing after the current character
a
# start typing before the current character
i
# start typing in a new line after the current line
o
# start typing in a new line before the current line
O
# start typing at the end of the current line
A
# start typing at the beginning of the current line
I
```

#### Deletion: <a name='del'></a>
```bash
# deletes the current character 
x
# replaces the current character
r
# deletes the character before the current character
X
# pastes the character deleted by x, X
p
# swap two character, cut and pase
xp
```

#### Undo and Redo: <a name='do'></a>
```bash
# undo the last operation / last change
u
# redo the last operation 
.
```

#### Cut, Copy, Paste: <a name='edit></a>
```bash
# cut the current line
dd
# copy the current line
yy
# paste the line after the current line
p
# paste the line before the current line
P
# delete `n` no.of lines below the current line
ndd # n = no. of lines (3dd)
# copy `n` no.of lines below the current line
nyy # n = no.of lines (3yy)
```

#### Navigation: <a name = "nav"></a>
```bash
# jump to the start of the current line
0
^
# jump to the end of the current line
$
# delete until the beginning of the line
d0 # preserves the current character
# delete untilt the end of the line
d$ # delets the current character also
```

#### Line Actions: <a name="line"></a>
```bash
# join the current line with the line below
J
# copy and paste the current line
yyp
nyyp # n = no.of lines
# switches the lines
ddp
nddp # n = no.of lines
```

#### Word Actions: <a name='word'></a>
```bash
# jump forward one word (ctrl + right in sublime)
w
# jump backward one word (ctrl + left in sublime)
b
```

#### Search Operations:<a name='search'></a>
```bash
# search the string forwards (top to bottom) in a file
:/{string} # searching for `printf`:  :/printf
# search the string backwards (bottom to top) in a file
:?{string} # searching for `printf`:  :?printf
# search for the string if its in the start of the line(s)
:/^{string} # searching for `echo` in beginning each line: /^echo
# search for the string if its in the end of the line(s)
:?{string}$  # searching for `close` in end each line: ?close$
# search using reg-ex value
:/xy[z123]a # matches xyza, xy1a, xy2a, xy3a of forward search
:?xy[z123]a  # matches xyza, xy1a, xy2a, xy3a of reverse search
```

#### Replace Operations:<a name='replace'></a>
```bash
# change all the occurance of a string in a specified lines
:/x,y s/{search}/{replace}/g # :/1,3 s/awk/cut/g -> replaces all occurances of awk with cut in line 1 to 3
# change the occurance from line 1 to end of the file
:/1,$ s/{search}/{replace}/g # :/1,$ s/awk/cut/g -> changes all the occurances of awk with cut in the file
# another way of searching and replacing the entire file
:%s/{search}/{replace}/g     # :%s/iam/echo/g -> changes all occurances of iam with echo
```

#### File Operations:<a name='file'></a>
```bash
# read a file and load its contents in the file
:r {path for the file} # :r /etc/passwd
# execute the command and include its output in the file
:r !{command} # :r !ls
# opening multiple files
vim file1 file2
# traversing between files
:ls # shows all the files in the buffer
:b{no} # :b2 -> jumps 
:bn # jumps to next file in the buffer
:bp # jumps to previous file in the buffer
:vs {file} # :vs /etc/passwd -> open the file and make a vertical split
:sp {file} # :sp /etc/passwd -> opens a file and makes a horizontal split
```


##### Reference:
A good reference cheatcheet comprising of most materials: [vim.rtorr.com](https://vim.rtorr.com/)
Printed format with some detailed explanations: [fprint](https://www.fprintf.net/vimCheatSheet.html)

