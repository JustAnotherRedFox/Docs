-------------- NVIM -------------
# LazyVim
| KEY |   | Description |			 | Mode |

> Modes	
	> n = normal Mode
		> ff = exit to n mode  			= i
	> i = insert Mode
		> i = insert on letter 			= n
		> o = insert 1 line below 		= n
		> O = insert 1 line above 		= n
		> A = insert on end of line 	= n 
	> v = visual Mode
	> v-b = Visual Block mode 
		> ctrl + v = enter visual block mode 
			> I = to insert text on all highlighted column
			> Esc + Esc = to apply 
> Keys
	> # = key placeholder
	> S- = Shift + #
	> C- = Ctrl + #
	> <L> = Leader Key + #
	
# [Movement Keys]
* h	= left  							= n 
* j	= up  								= n 
* k = down  							= n 
* l	= right 							= n 
* w = next word 						= n 
* b = next word 						= n
* W = prev big word
* B = prev big word
* :# = Go to # Line						= n

# [Movement inside File]
* G = end of the file					= n
* gg = top of the file					= n
* e = end of the word					= n
* 0 = start of the line					= n
* $ = end of the line					= n
* } = end of the paragraph				= n
* % = end of brackets					= n
* zz = centralize verticaly				= n
* * = search for word under cursor 		= n

# [Movement Windows]
* C-h	= left window 					= n  
* C-j	= lower window  				= n 
* C-K	= upper window  				= n 
* C-l	= right window  				= n 
* <L>-  = split window below    		= n 
* <L>|  = split window right 			= n

# [Movement Buffer(aka. tab)]
* S-h   = prev buffer(tab) 				= n 
* S-l 	= next buffer(tab) 				= n 

# [Surrounding]
* gza  = creating a surrounding  		= v
	* e.g surround a word with '{}'

# [Changing Text]
* cw	= change the word from the cursor to the end of word
* ci( 	= change text inside current brackets 
* ci{   = change text inside current curly braces
* ci'	= change text inside current ' quotes
* ci"	= change text inside current " quotes
* r<char> = Replaces character under cursor

-------------------------- vim ------------------------
normal mode: ESC, jj
insert mode: i, I, a, A, o, O
visual mode: v
  CMD  mode: :
# comment
* gcc  		'comment/uncomment a line'
* gc 		'comment/uncomment a selection(in V mode)'



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
