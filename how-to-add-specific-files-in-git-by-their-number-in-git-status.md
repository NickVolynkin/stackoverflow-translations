# Example repo:
I'm using an example repo with four files: a, b, c, d.  
Here `a` is tracked, changed and staged; `b` is tracked, changed and not staged; `c` in untracked and staged; `d` is just untracked.

![enter image description here][1]
# External tool: [git-number][2]

> When run without arguments, 'git number' runs 'git status' and attach a unique number for each line of filename printed by 'git status', and it will 'remember' this number-to-filename association. When run with arguments, like this:

    $ git number <any git command> [one or more numbers or git options/args]

>'git number' will run that <any git command> and subtitute all the numbers to their equivalent filenames. Non-numeric argument are passed intact to git.

![enter image description here][3]

This is available with other commands.

![enter image description here][4]

# External tool: [SCM Breeze][5]

> SCM Breeze is a set of shell scripts (for bash and zsh) that enhance your interaction with git. It integrates with your shell to give you numbered file shortcuts, a repository index with tab completion, and many other useful features.

SCM Breeze utilizes keyboard shortcuts and aliases to work with git files by number:

<kbd>Ctrl</kbd> + <kbd>x</kbd>, <kbd>c</kbd> => `git_add_and_commit` - add given files (if any), then commit staged changes

<kbd>Ctrl</kbd> + <kbd>x</kbd>, <kbd>Space</kbd> => `git_commit_all` - commit everything


`git add`:

    $ ga 1

`git diff`:

    $ gd 2

`git reset`:

    $ grs 3

`git commit`:

    $ gco 4

# Native way with `git add -i`

    git add -i

From [Git reference][6]:
> **-i**  
> **--interactive**  
> Add modified contents in the working tree interactively to the index. Optional path arguments may be supplied to limit operation to a subset of the working tree. See “Interactive mode” for details.

You can remember this as `-i`ntuitive, because the interface is really intuitive. Well, at least to hardcore Vim users.

Opening the interactive mode:
![enter image description here][7]

Adding (staging) a tracked file:
![enter image description here][8]

Adding an untracked file:
![enter image description here][9]

See the changes:
![enter image description here][10]

If you're stuck in the middle of adding, hit <kbd>Return</kbd> with an empty string.


**Note:**

If you're confused with the appearance and coloring: I've been using [iTerm2][11] + [zsh][12] + [oh-my-zsh][13].


  [1]: http://i.stack.imgur.com/XmH5P.png
  [2]: https://github.com/holygeek/git-number
  [3]: http://i.stack.imgur.com/BceGK.png
  [4]: http://i.stack.imgur.com/B7lj0.png
  [5]: https://github.com/ndbroadbent/scm_breeze
  [6]: http://www.git-scm.com/docs/git-add
  [7]: http://i.stack.imgur.com/GUAxo.png
  [8]: http://i.stack.imgur.com/62E6D.png
  [9]: http://i.stack.imgur.com/XNcsU.png
  [10]: http://i.stack.imgur.com/kAky1.png
  [11]: https://iterm2.com/
  [12]: http://www.zsh.org/
  [13]: https://github.com/robbyrussell/oh-my-zsh
