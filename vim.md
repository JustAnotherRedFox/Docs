-------------------------- vim ------------------------
normal mode: ESC, jj
insert mode: i, I, a, A, o, O
visual mode: v
  CMD  mode: :
# comment
* gcc  		'comment/uncomment a line'
* gc 		'comment/uncomment a selection(in V mode)'
movimentation(normal mode) :
h: left
j: down
k: up
l: right

G: end of the file
gg: top of the file
e: end of the word
w: start of the next word
0: start of the line
$: end of the line
}: end of the paragraph
%: end of brackets, square brackets, curly brackets

insertion movimentation:

I: insertion in start of the line
a: insertion one letter in front of the cursor
A: insertion in the end of the line
o: insertion and create one line below
O: insertion and create one line above

x: delete the letten selected
X: delete the letter behide
dd: delete the whole line

y: copy
p: paste
yy: copy a whole line
x,dd...: can be use as cut command

u: undo the last modification
U: undo a whole line of modifications
ctrl + R: redo the undo

search:
in normal mode  /search_item
ex.: /delete
	* will search by delete
	* use n to next
	* use N to previous

:q  - quit without save
:q! - force quit without save
:w  - save 
:wq - write and quit

:w new_name - to save with a new name
