# Демонстрационный репозиторий:
Для примеров я использую репозиторий с четырьмя файлами: a, b, c, d.  
Из них `a` - отслеживается, изменен, добавлен (tracked, changed and staged); `b` отслеживается, изменен, но не добавлен (tracked, changed and not staged); `c` не отслеживается, но добавлен; `d` просто ещё не отслеживается.

![enter image description here][1]
# Отдельная утилита: [git-number][2]

При запуске без аргументов, `git number` выполняет обычный `git status`, добавляя уникальный номер каждой выводимой строке с именем файла. Он "запоминает" соответствие номера файлу.

При запуске с аргументами:


    $ git number <любая команда git> [одно или несколько чисел, и/или --аргументов]
    
`git number` запускает эту <любую команду>, заменяя все числа соответствующими именами файлов. Нечисловые аргументы передаются в git без изменений.

![enter image description here][3]

Прпмер с командой `diff` :

![enter image description here][4]

# Отдельная утилита: [SCM Breeze][5]

SCM Breeze - это набор shell-скриптов для bash и zsh. Он дает новые возможности работы с Git. Он интегрируется в вашу командную оболочку и добавляет упоминание файла по номеру, индекс репозитория с автодополнением по <kbd>Tab</kbd> и многие другие функции.

SCM Breeze использует горячие клавиши и псевдонимы (aliases) команд:

<kbd>Ctrl</kbd> + <kbd>x</kbd>, <kbd>c</kbd> => `git_add_and_commit` - добавить выбранные файлы и сделать коммит всех добавленных изменений.

<kbd>Ctrl</kbd> + <kbd>x</kbd>, <kbd>Space</kbd> => `git_commit_all` - сделать коммит всех имеющихся изменений.


`git add`:

    $ ga 1

`git diff`:

    $ gd 2

`git reset`:

    $ grs 3

`git commit`:

    $ gco 4

# "Родными" средствами: `git add -i`

    git add -i

Из [Git reference][6]:
> **-i**  
> **--interactive**  
> Добавить содержимое рабочей папки в индекс в интерактивном режиме...

Этот режим можно запомнить как `-i`нтуитивный, поскольку он невероятно понятен и удобен (по крайней мере, для бывалого пользователя Vim).

Входим в интерактивный режим:
![enter image description here][7]

Добавляем измененный отслеживаемый файл:
![enter image description here][8]

Добавляем неотслеживаемый файл:
![enter image description here][9]

Смотрим на результат:
![enter image description here][10]

Если не можете выйти из режима добавления, нажмите <kbd>Return</kbd> с пустой строкой.


**Note:**

Если вам интересно, что это за консоль/цвета/оформление: [iTerm2][11] + [zsh][12] + [oh-my-zsh][13].


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
