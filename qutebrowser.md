# Movement
* j		'scroll current page one line up'
* k		'scroll current page one line down'
* h		'scroll current page left'
* l		'scroll current page right'

* G		'scroll to bottom of current page'
* gg 			'scroll to top of current page'
* Ctrl + f 		'scroll current page one screen down'
* Ctrl + B 		'scroll current page one screen up'

* /				'Open the search forward prompt'
* ? 	'Open the search Backward prompt'

# Zoom
* +			 	'Zoom in current page'
* - 			'Zoom out current page'
* = 			'Default Zoom'

# Browser Modes
* i 		'Insert Mode, input as text'
* v 		'Visual Mode, Selection and highlight of text'
* ESC 		'Normal Mode, Input as cmd'

# Copy and Loading
> clipboard works on current context(window, tab), selectin buffer allow to transfer between contex(from browser to terminal)
* y 		'copy current selected text(in v mode) to clipboard'
* Y 		'copy current selected text(in v mode) to selection buffer'
	* e.g coping from browser and past on terminal
	* v 			'to enter V mode'
	* v 			'type v again to enter select mode'
	* l, h or h 	'to highlight/select text(h/l select char by char, w select word by word)'
	* Y 			'to copy to selection buffer the highlighted text'

* yy 		'Copy current page URL to clipboard'
* yt 		'Copy current page title to clipboard'
* yY 		'Copy current page URL to selection buffer'
* yT 		'Copy current page title to selection buffer'

* pp		'Load URL in clipboard'
* pP 		'Load URL in selection buffer'
* Pp 		'Load URL in clipboard on new tab'
* PP 		'Load URL in selection buffer on new tab'

* wp 		'Load URL in clipboard on new window'
* wP 		'Load URL in selection buffer on new window'

# History Navegation
* H 		'Go back to previous web page'
* L 		'Go forward to next web page'
* th        'Go Back to previous web page and open on new tab'
* tl 		'Go forward to next web page and open on new tab'

# Tab management
* alt + n 	'go to numbered tab e.g alt + 2, moves to tab 2'
* d 		'Close current tab'
* go 		'open url and edit it'
* xo 		'open a blank url and open it on backgroud tab'
* gC 		'duplicate current tab'
* co 		'close all backgroud tabs'
* Ctrl + h  'load homepage'
* Ctrl + s  'stop loading a page'
* gd 		'save current page to file'
* sk 		'create a new keybinding
* sf 		'save current cofiguration to a file'
* Ss 		'open setting page for qutebrowser'
* Ctrl + q  'exit browser'

# Bookmarking
* Sq 		'show bookmarks and quickmarks list'
* m 		'save current page as quickmark'
* M 		'save current page as bookmark'
* b 		'load a quickmark'
* B 		'load a bookmark'
* wb 		'load a quickmark on new window'
* wB 		'load bookmark on new window'

# command mode
* :history 	'display current browsing history'
* 