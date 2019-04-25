# Vim Editor Commands

Vim is an editor to create or edit a text file.

There are two modes in vim. One is the command mode and another is the insert mode.

In the command mode, user can move around the file, delete text, etc.

In the insert mode, user can insert text.

## Changing mode from one to another

From command mode to insert mode	type `a/A/i/I/o/O ` (see details below)

From insert mode to command mode	type <kbd>esc</kbd> (escape key)

Some useful commands for VIM

### Text Entry Commands (Used to start text entry)

<kbd>a</kbd> Append text following current cursor position

<kbd>A</kbd> Append text to the end of current line

<kbd>i</kbd> Insert text before the current cursor position

<kbd>I</kbd> Insert text at the beginning of the cursor line

<kbd>o</kbd> Open up a new line following the current line and add text there

<kbd>O</kbd> Open up a new line in front of the current line and add text there

### The following commands are used only in the commands mode

**Cursor Movement Commands**

<kbd>h</kbd> Moves the cursor one character to the left

<kbd>l</kbd> Moves the cursor one character to the right

<kbd>k</kbd> Moves the cursor up one line

<kbd>j</kbd> Moves the cursor down one line

<kbd>line number</kbd> + <kbd>G</kbd> or :n Cursor goes to the specified (n) line (ex. 10G goes to line 10)

<kbd>⌃ Control</kbd> + <kbd>F</kbd> Forward screenful

<kbd>⌃ Control</kbd> + <kbd>B</kbd> Backward screenful

<kbd>⌃ Control</kbd> + <kbd>F</kbd> One page forward

<kbd>⌃ Control</kbd> + <kbd>b</kbd> One page backward

<kbd>⌃ Control</kbd> + <kbd>U</kbd> Up half screenful

<kbd>⌃ Control</kbd> + <kbd>D</kbd> Down half screenful

<kbd>$</kbd> Move cursor to the end of current line

<kbd>0</kbd> (zero) Move cursor to the beginning of current line

<kbd>w</kbd> Forward one word

<kbd>b</kbd> Backward one word

**Exit Commands**

`:wq` Write file to disk and quit the editor

`:q!` Quit (no warning)

`:q` Quit (a warning is printed if a modified file has not been saved)

`ZZ` Save workspace and quit the editor (same as `:wq`)

`: 10,25 w temp` write lines 10 through 25 into file named temp. Of course, other line. Numbers can be used. (Use `:f` to find out the line numbers you want.

**Text Deletion Commands**

<kbd>x</kbd> Delete character

<kbd>d</kbd> + <kbd>w</kbd> Delete word from cursor on

<kbd>d</kbd> + <kbd>b</kbd> Delete word backward

<kbd>d</kbd> + <kbd>d</kbd> Delete line

<kbd>d</kbd> + <kbd>$</kbd> Delete to end of line

<kbd>d</kbd> + <kbd>^</kbd> (caret, not CTRL) Delete to beginning of line

**Yank** (has most of the options of delete) - VI's copy commmand

<kbd>y</kbd> + <kbd>y</kbd> yank current line

<kbd>y</kbd> + <kbd>$</kbd> yank to end of current line from cursor

<kbd>y</kbd> + <kbd>w</kbd> yank from cursor to end of current word

<kbd>number</kbd> + <kbd>y</kbd> + <kbd>y</kbd> yank, for example, 5 lines (<kbd>5</kbd> + <kbd>y</kbd> + <kbd>y</kbd>)

**Paste** (used after delete or yank to recover lines)

<kbd>p</kbd> paste below cursor

<kbd>P</kbd> paste above cursor

<kbd>"</kbd> + <kbd>number</kbd> + <kbd>p</kbd> paste from buffer (there are 9)

<kbd>u</kbd> Undo last change

<kbd>U</kbd> Restore line

<kbd>J</kbd> Join next line down to the end of the current line

**File Manipulation Commands**

`:w` Write workspace to original file

`:w` file Write workspace to named file

`:e` file Start editing a new file

`:r` file Read contents of a file to the workspace

**To create a page break**, while in the insert mode, press the <kbd>⌃ Control</kbd> key and <kbd>l</kbd>. `⌃L` will appear in your text and will cause the printer to start a new page.


**Other Useful Commands**

Most commands can be repeated _n_ times by typing a number, _n_, before the command. For example `10dd` means delete 10 lines.

<kbd>.</kbd> Repeat last command

<kbd>c</kbd> + <kbd>w</kbd> Change current word to a new word

<kbd>r</kbd> Replace one character at the cursor position

<kbd>R</kbd> Begin overstrike or replace mode. Use <kbd>esc</kbd> key to exit

`:/` pattern Search forward for the pattern

`:?` pattern Search backward for the pattern

<kbd>n</kbd> (used after either of the 2 search commands above to
continue to find next occurrence of the pattern).

`:g/pat1/s//pat2/g` replace every occurrence of pattern1 `(pat1)` with `pat2`

*Example* `:g/tIO/s//Ada.Text_IO/g`

This will find and replace `tIO` by `Ada.text_IO` everywhere in the file.

`:g/a/s// /g` replace the letter a, by blank

`:g/a/s///g` replace a by nothing

_note: Even this command be undone by <kbd>u</kbd>_


## Examples

### Opening a New File

**Step 1**	type	`vim filename` 	(create a file named filename)

**Step 2**	press	<kbd>i</kbd>	( switch to insert mode)

**Step 3**	enter text (enter your Ada program)

**Step 4**	hit <kbd>esc</kbd> key	(switch back to command mode)

**Step 5**	`:wq`	(write file and exit Vim)

### Editing the Existing File

**Step 1** type	`vim filename`	(edit the existing file named filename)

**Step 2**	move around the file using `h/j/k/l` key or any appropriate command

<kbd>h</kbd> Moves the cursor one character to the left

<kbd>l</kbd> Moves the cursor one character to the right

<kbd>k</kbd> Moves the cursor up one line

<kbd>j</kbd> Moves the cursor down one line

<kbd>number</kbd> + <kbd>G</kbd> or `:n Cursor` goes to the specified (n) line (ex. 10G goes to line 10)

**Step 3**	edit required text (replace or delete or insert)

**Step 4**	hit <kbd>esc</kbd> key (exit from insert mode if you insert or replace text)

**Step 5** `:wq`
