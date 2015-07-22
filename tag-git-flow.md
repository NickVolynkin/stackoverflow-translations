
Git flow включает в себя набор базовых правил относительно того, как различные процессы в разработке сопровождаются с помощью ветвей ([tag:git-branch]) и операций с ними в [tag:git].

Кратко:

  * Главная ветвь `origin/master`, исходный код в которой всегда является полностью рабочим. [tag:merge] в `master` - это, как правило, релиз очередной стабильной версии.

  * Главная ветвь разработки `origin/develop`, куда сливаются законченные версии функциональностей. 
  * Ветви функциональностей - `feature/...`
  * Ветви релизов - `release/...`
  * Ветви исправлений - `hotfix/...`


Модель Git flow была представлена в статье Vincent Driessen [A successful Git branching model][1]. На русском языке можно прочитать:

* http://habrahabr.ru/post/106912/
* http://demiazz.github.io/blog/2011/11/19/a-successfull-git-branching-model/

Реализация [tag:git-flow] может выполняться вручную, но удобнее будет использовать специальные инструменты, дополняющие [tag:git]:

* https://github.com/nvie/gitflow
* https://github.com/petervanderdoes/gitflow


![git-flow illustration][2]


  [1]: http://nvie.com/posts/a-successful-git-branching-model/
  [2]: http://i.stack.imgur.com/7Culm.png
