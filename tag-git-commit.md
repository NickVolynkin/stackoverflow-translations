`git commit` – это команда Git для записи индексированных изменений в репозиторий. Используйте эту метку для обозначения всех вопросов, связанных с созданием, редактированием и внутренней структурой коммитов в Git.

----
## Общие сведения

`git commit` - это команда для записи индексированных изменений в репозиторий Git.

Прежде чем создавать очередной коммит, необходимо проиндексировать файлы в рабочей области с помощью команды [tag:git-add]. Новый коммит будет включать текущие состояния индексированных файлов плюс последние сохраненные состояния неиндексированных (но отслеживаемых) файлов. Обратите внимание: коммит включает в себя не изменения (дельты, патчи) относительно предыдущего коммита, а "снимок" (англ. shapshot) текущего состояния рабочей области.

Каждому коммиту соответствует код, создаваемый Git по алгоритму [Secure Hash Alrorithm 1][1]. Он зависит от содержимого коммита, автора и времени создания. Таким образом, коммит с тем же содержимым, созданный в другое время, имеет другой `sha1`. Git использует `sha1` для того, чтобы различать коммиты (и другие объекты) между собой.

## Использование

Создать новый коммит:

    git commit -m'сообщение'

Включить новые изменения в последний созданный коммит

    git commit --amend [-m'сообщение']

Не создавать коммит, а только показать отчет и детальную информацию о нем, как если бы он был создан. (Используется для проверки на ошибки перед реальным коммитом).

    git commit --dry-run

Показать сведения о последних выполненных коммитах:

    git log

## Часто задаваемые вопросы

* http://ru.stackoverflow.com/questions/418866/
* http://ru.stackoverflow.com/questions/359475/
* http://ru.stackoverflow.com/questions/414158/
* http://ru.stackoverflow.com/questions/216804/

## Рекомендуемые к прочтению вопросы

* http://ru.stackoverflow.com/questions/418913/
* http://ru.stackoverflow.com/questions/126895/
* http://ru.stackoverflow.com/questions/363133/

## Документация

В русскоязычной документации используются следующие термины:

* to commit - выполнить коммит (можно "закоммитить", но только в устной речи, не в документации)
* commit - коммит
    
### На русском языке:

1. [Pro Git на русском, глава 2.2][2] 

### На английском языке:

2. [Git reference: `git commit`][3]


  [1]: https://ru.wikipedia.org/wiki/SHA-1
  [2]: http://www.git-scm.com/book/ru/v1/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%97%D0%B0%D0%BF%D0%B8%D1%81%D1%8C-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9-%D0%B2-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B9
  [3]: http://www.git-scm.com/docs/git-commit
  
