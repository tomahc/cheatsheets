# vim

## Copying and Moving Text

### display registers
```
:reg[isters]
:di[splay]
```

### yank into register

cmd | decription
--------------------|---------------------
["x]yy				| copy whole line in register
["x]Y				| yank [count] lines into register
{visual}["x]y		| visual yank into register

### paste from register

cmd | decription
------------------|---------------------
["x]p			  | paste register after the cursor [count] times
["x]P			  | paste register before the cursor [count] times 
["x]gp			  | like "p" but leave cursor after the new text
:[line]pu[t] [x]  | Put the text [from register x] after [line] (default current line
:[line]pu[t]! [x] | Put the text [from register x] before [line] (default current line).


### Undo/Redo/Repeat

cmd | decription
----------------|---------------------
u				| Undo [count] times
:u[ndo]			| Undo one change
CTRL-R			| Redo [count] changes which were undone
:red[o]			| Redo one change which was undone
U				| Undo all latest changes on one line
.				| Releat last change, with count replaced with [count]


### Moving Around

##### A word consists of a sequence of letters, digits and underscores, or a sequence of other non-blank characters, separated by whitespaces (\s, \t, ... ).
##### A WORD consists of a sequence of non-blank characters, separated by whitespaces. An empty line is also considered to be a word and a WORD.

cmd | decription
----------------|---------------------
e				| Forward to the end of word [count]
E				| Forward to the end of WORD [count]
(				| [count] sentences backwards
)				| [count] sentences forward
{				| [count] paragraphs backwards
}				| [count] paragraphs forward

### Window splitting and focusing

cmd | decription
----------------|---------------------
:vsplit			| split vertically
:split			| split horizontally
:ar				| list all open files
CTRL-w			| focus next window (cycling)