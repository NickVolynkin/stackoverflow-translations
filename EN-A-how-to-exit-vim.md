http://stackoverflow.com/a/30710567/2790048

Before you enter a command, **hit the <kbd>Esc</kbd> key**. After you enter it, hit the <kbd>Return</kbd> to confirm.

<kbd>Esc</kbd> switches Vim to [command-line mode][1].   Now if you press <kbd>:</kbd>, the `:` will appear at the *bottom* of the screen. This confirms that you're actually typing a command and not editing the file. 

Most commands have abbreviations, with optional part enclosed in brackets: `c[ommand]`.

Commands marked with '*' are Vim-only (not implemented in Vi).

**Safe-quit (fails if there are unsaved changes):**

*  `:q[uit]`  Quit the current [window][2]. Quit Vim if this is the last		window.  This fails when changes have been made in current [buffer][3].
*  `:qa[ll]`*  Quit all windows and Vim, unless there are some buffers which have been changed.


**Prompt-quit (prompts if there are unsaved changes)**

* `:conf[irm] q[uit]`* Quit, but give prompt when there are some buffers which have been changed.
* `:conf[irm] xa[ll]`* Write all changed buffers and exit Vim. Bring up a prompt when some buffers cannot be written.

**Write (save) changes and quit:**

* `:wq` Write the current file (even if it was not changed) and quit.  Writing fails when the file is read-only or the buffer does not have a name. `:wqa[ll]`* for all windows.
* `:wq!` The same, but writes even read-only files. `:wqa[ll]!`* for all windows.
* `:x[it]`, `ZZ`(with [details][4]). Write the file only *if it was changed* and quit, `:xa[ll]`* for all windows.

**Discard changes and quit:**

* `:q[uit]!` `ZQ`* Quit without writing, also when visible buffers have changes.  Does not exit when there are changed hidden buffers. 
* `:qa[ll]!`\*, `:quita[ll][!]`* Quit Vim, all changes to the buffers (including hidden) are lost.

**Press <kbd>Return</kbd> to confirm the command.**

This answer doesn't reference all Vim write and quit commands and arguments. Indeed, they are referenced in the [Vim documentation][5]. 

Vim has extensive built-in help, type <kbd>Esc</kbd>`:help`<kbd>Return</kbd> to open it.

<sub>
This answer was inspired by the [other one][6], originally authored by @dirvine and edited by other SO users. I've included more information from Vim reference, SO comments and some other sources. Differences for Vi and Vim are reflected too.
</sub>

  [1]: http://vimdoc.sourceforge.net/htmldoc/cmdline.html#Command-line
  [2]: http://vimdoc.sourceforge.net/htmldoc/windows.html#window
  [3]: http://vimdoc.sourceforge.net/htmldoc/windows.html#buffers
  [4]: http://vimdoc.sourceforge.net/htmldoc/editing.html#ZZ
  [5]: http://vimdoc.sourceforge.net/htmldoc/editing.html#:q
  [6]: http://stackoverflow.com/a/11828573/2790048