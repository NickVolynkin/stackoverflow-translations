Question:
### How to add specific files in git by their number in git status?
http://stackoverflow.com/questions/30411901/how-to-add-specific-files-in-git-by-their-number-in-git-status

Answer:


### Native way

    git add -i

From [Git reference][1]:
> **-i**  
> **--interactive**  
> Add modified contents in the working tree interactively to the index. Optional path arguments may be supplied to limit operation to a subset of the working tree. See “Interactive mode” for details.

### External tool way

https://github.com/holygeek/git-number

> When run without arguments, 'git number' runs 'git status' and attach a unique number for each line of filename printed by 'git status', and it will 'remember' this number-to-filename association. When run with arguments, like this:

    $ git number <any git command> [one or more numbers or git options/args]


>'git number' will run that <any git command> and subtitute all the numbers to their equivalent filenames. Non-numeric argument are passed intact to git.

  [1]: http://www.git-scm.com/docs/git-add
