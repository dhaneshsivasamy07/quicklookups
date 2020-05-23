Normal Mode = You open the file and start editing in Vim <br />
Command Mode = You open the file to ed edited and press ```esc``` key
                                                                                                                                                        
# _Normal mode Operations_                                                                                                                                       
### INSERT OPERATIONS
a               =       type(insert) after the current char <br />
i               =       type(insert) before the current char <br />
o               =       type(insert) on a new line after the current line <br />
A               =       type(insert) at the end of the crrent line <br />
I               =       type(insert) at the start the current line <br />
O               =       type(insert) on a new line after the current line <br />
                                                                                                                                                        
### DELETE AND REPLACE OPERATIONS                                                                                                                 
x               =       deletes the character below the cursor <br />
r (string)      =       replaces the char under the cursor with the typing one <br />
X               =       deletes the character before the cursor <br />
p               =       pastes the last character that us removed (by x and X) <br />
xp              =       switch two characters <br />

### UNDO and REPEAT OPERATIONS
u               =       undo the last operation <br />
.               =       redo the last operation <br />

### CUT COPY PASTE OPERATIONS
dd              =       cut the current line <br />
yy              =       copy the current line <br />
p               =       paste after the current line <br />
P               =       paste before the current line <br />
3dd             =       deletes three lines below the cursor <br />
4yy             =       copies four lines below the cursor <br />

### NAVIGATION OPERATIONS
0/^             =       jumps to the start of the current line <br />
$               =       jumps to the end of the current line <br />
d0              =       delete until the start of the line (leaves the char under the cursor) <br />
d$              =       delete until the end of the line <br />

### LINE ACTIONS
J               =       joins the current line with the below line <br />
yyp             =       duplicate the current line (copy and paste) <br />
ddp             =       switch lines (deletes the line and pastes it under the current line) <br />

### WORD ACTIONS
w               =       jumps forward one word <br />
b               =       jumps backward one word <br />
int w           =       jumps forward int words <br />
int b           =       jumps backward int words <br />

# _Command mode Operations_
### SEARCH OPERATIONS
:/string                =       searches for the entered string (forward) <br />
:?string                =       searches for the entered string (backward) <br />
:/^string       =       searches if the entered string is present at the start of the line <br />
:?^string       =       searches if the entered string is present at the end of the line <br />
:/xy[z123]a     =       searches for xyza, xy1a, xy2a, xy3a, for backward search use ? instead of / <br />
:n              =       moves to the next occurances of the searched string <br />

### REPLACE OPERATIONS
:/4,8 s/test/TEST/g     =       replaces test with TEST from line 4 to 8 <br />
:/1,$ s/test/TEST/g     =       replaces test with TEST from all the lines <br />

### READ FILES OPERATIONS
:r file         =       includes the contenets of the file in the current file <br />
:r !cmd                 =       the command is executed and the output is included in the file <br />

### MULTIPLE FILE ACCESSING OPERATIONS
vi test test2 test3     =       opens 3 files <br />
:args                   =       lists the opened files and marks the active one <br />
:n                      =       moves to the next file <br />
