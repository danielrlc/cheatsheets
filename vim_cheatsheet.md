Vim cheatsheet
--------------

Help
--------------------------------------------------------------------------------

C-]                   | Jump to tag under cursor (useful in help)
:h window             | Bring up help for "window"



Working with files
--------------------------------------------------------------------------------

vi text1.md           | Open text1.md in Vim
ZZ or :wq             | Write changes and exit Vim
:saveas ~/some/path/  | Save your file to that location
:q!                   | Get out of Vim without saving changes



Netrw
--------------------------------------------------------------------------------

:help netrw           | Open help for netrw
:e[dit].              | Open netrw at current working directory
:vs[plit].            | Open netrw in split at current working directory #use
:E[xplore]            | Open netrw at directory of current file
:Se[xplore]           | Open netrw in split at directory of current file
:Vex[plore]           | Open netrw in vertical split at directory of current file
%                     | Create a new file #use
d                     | Create a new directory
x                     | Open file in default editor (VS Code?)



Autocompletion
--------------------------------------------------------------------------------

C-n                   | Cycle forward through autocomplete options #use
C-p                   | Cycle back through autocomplete options
C-x C-l               | Auto-complete line, cycling through possibilities #use



Move around file
--------------------------------------------------------------------------------

C-d                   | Go down half a page #use
C-u                   | Go up half a page #use
100gg                 | Go to line 100
C-g                   | See current line number etc at bottom of screen
C-o                   | Cycle back through recent positions #use
C-i                   | Cycle forward through recent positions #use
%                     | Go to matching bracket #use
H, M, L               | Go to High, Middle, Low position on screen



Line editing
--------------------------------------------------------------------------------

U                     | Undo all recent changes for current line
;                     | Repeat last f/t/F/T command
,                     | Repeat last f/t/F/T command in other direction
gqq                   | Format line, enforcing max character width (eg 80)
gqap                  | Format current paragraph
gqG                   | Force character width (eg 80) for all lines in file
                      | But take care! Messes with ``` sections.


Windows management
--------------------------------------------------------------------------------

C-w w                 | Cycle through windows
C-w hjkl              | Go to window to left/down/up/right
C-w HJKL              | Move window left/down/up/right
:vnew                 | Open a new window beside the current window
:vs[plit] text1.md    | Edit text1.md in new window beside current window #use
:vert h tabnew        | Pull up help for tabnew in vertical split #use



Tabs management
--------------------------------------------------------------------------------

:tabnew               | Open a new tab #use
:tabedit text1.md     | Edit text1.md in a new tab #use
C-w T                 | Break the current window out to a new tab #use



Command mode
--------------------------------------------------------------------------------

:e C-d tab space      | Cycle through commands starting with "e" #use
<Space>/              | Toggle 'hlsearch' (custom) #use



Find and replace
--------------------------------------------------------------------------------

:s/old/new/g          | Change all in line
:%s/old/new/g         | Change all in file #use
:%s/old/new/gc        | Change all in file, confirming each time #use



File management
--------------------------------------------------------------------------------

:w test1.md           | Write to (new) test1.md file



Copying and pasting
--------------------------------------------------------------------------------

:'<,'>w test1.md      | Save highlighted text to (new) test1.md file
:r test1.md           | Paste in contents of text1.md
:r !ls                | Paste in ls command output
yyp V r -             | Underline a heading #use



Odds and ends
--------------------------------------------------------------------------------

ea                    | Start appending text to word under cursor #use
R                     | Replace text under cursor #use
dw 5.                 | Delete word, then delete five more words



Commands + text objects
--------------------------------------------------------------------------------

:&                     | Repeat the last ex command
:h motion             | Pull up Vim's help page for motions
:h text-objects       | Pull up Vim's help page for text objects
:>ip                   | Indent inside paragraph
=ip                   | Sort out indenting paragraph(???)
dip                   | Delete paragraph
cib                   | Change inside (some???) brackets
:dat                   | Delete a whole tag (eg an HTML tag)
cit                   | Change inside tag
=                     | Reformat (reindent, break long lines, etc)
dj                    | Delete down a line (current and one below)
d/world               | Delete up until the first search match for "world"



Visual block mode
--------------------------------------------------------------------------------

C-v                   | Enter visual block mode
r                     | Replace all characters with the next character you type
I                     | Insert text before the block
A                     | Insert text after the block



Surround.vim plugin
--------------------------------------------------------------------------------

:ds"                   | Delete surrounding "
cs<old><new>          | Replace surrounding old character with new character
ys<text-obj><newchar> | Surround text-object with <newchar>
yss<li>               | Surround line with <li>
cst<li>               | Change surrounding tag to <li>
dst                   | Delete surround tag (works on HTML tags)



Emmet plugin
--------------------------------------------------------------------------------

C-y ,                 | Apply expansion
html:5                | Create HTML5 boilerplate



Fzf plugin
--------------------------------------------------------------------------------

C-j                   | Navigate down in search matches
C-k                   | Navigate up in search matches
