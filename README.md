Репозитарий для тренировки с git.

Краткая шпрагалка по git и GitHub   

git - это система контроля версий. Разработал и создал Линус Торвальдс, создатель "Линукс".  
GitHub - это популярный удаленный репозитарий, к котором храниться большое количество проектов в IT. Принадлежит компании "Майкрософт".  


1. Начнем с GitHub  https://github.com

GitHub — сервис онлайн-хостинга репозиториев, обладающий всеми функциями распределённого контроля версий и функциональностью управления 
исходным кодом — всё, что поддерживает Git и даже больше. Также GitHub может похвастаться контролем доступа, багтрекингом, управлением 
задачами и вики для каждого проекта.  (источник - https://tproger.ru/translations/difference-between-git-and-github)

Сделать свой репозиторий на GitHub можно on-line, ссылка https://github.com. Для этого нужно пройти процедуру регистрации, создать логин, 
определить пароль и далее в совем аккаунте на GitHub можно создавать отдельные репозитории по определенным темам или направления, или в той 
логике, как считает владедец аккаунта. Загружать файлы в репозитории можно также online.    

В самом упрощеном случае, если репозиторий использует только владелец и не нужен контроль версий, то можно просто добавлять файлы (проекты) 
в репозиторий и если есть необходимость делиться ими. Т.е. по сути это будет облачное хранилище. Ограничения по хранению: 
на размер одно файла - 100Mb (рекоменуется до 50 Mb), на 1 репозиторий - 5Gb (рекоменуется 1 Gb)   

Для организации контроля версий, соединения с локальным репозиторием, совместной работы над файлами (проектами) нужно использовать git.  

Конкретное пояснение как работать с GitHub можно посмотреть по ссылке   
https://skillbox.ru/media/code/chto-takoe-github-i-kak-im-polzovatsya/


2. git - система контроля версий   

Терминология (источник - https://githowto.com/ru/git_basics)   

**Репозиторий**  
Репозиторий Git — это хранилище, в котором расположен ваш проект и его история. Это может быть локальное хранилище где-то на вашем 
компьютере или удаленное хранилище на сервисе типа GitHub или другом хостинге в Интернете. Репозиторий служит для отслеживания изменений 
в проекте, координации работы между несколькими людьми и отслеживания истории проекта.    

Скажем, у вас на компьютере есть директория со всеми файлами вашего проекта. Когда вы инициализируете репозиторий Git в этой директории, 
Git создает скрытую поддиректорию под названием .git, в которой хранится вся информация о репозитории. Эта информация включает историю 
всех изменений, внесенных в репозиторий, а также его текущее состояние.    

**Коммит**   
Вы можете думать о коммите как о снимке вашего проекта в определенный момент времени. Правда, коммит содержит только информацию об 
изменениях, которые были внесены в репозиторий с момента последнего коммита. Он не содержит все файлы репозитория 
(если только это не первый коммит). Таким образом, каждый коммит — это небольшой кусочек истории репозитория, основанный на 
предыдущем коммите. Все они связаны между собой в цепочку, формируя историю изменений вашего проекта.

**Ветка**   
Ветка — это параллельная версия репозитория. Ветки позволяют вам работать над отдельными функциями вашего проекта, не влияя на 
основную версию. Закончив работу над новой фичей, вы можете объединить эту ветку с основной версией проекта.   

Установить git (источники)  
https://git-scm.com/downloads   
https://gitforwindows.org   

Конкретное пояснение как работать с git можно посмотреть по ссылке
https://skillbox.ru/media/code/chto_takoe_git_obyasnyaem_na_skhemakh/?utm_source=media&utm_medium=link&utm_campaign=all_all_media_links_links_articles_all_all_skillbox
   
Хороший гайд: кратко теория + практический тренажер  
https://githowto.com/ru   

Шпаргалка по основным командам git  
https://github.com/cyberspacedk/Git-commands

Статья на Хабр "30 основных команд git"
https://habr.com/ru/companies/ruvds/articles/599929/

Информация по различным блокам:

Хеш — идентификатор коммита
	Информация о коммите — это набор данных: когда был сделан коммит, содержимое файлов в репозитории на момент коммита и ссылка на 
	предыдущий, или родительский (англ. parent), коммит. Git хеширует (преобразует) информацию о коммите с помощью алгоритма SHA-1 
	от англ. Secure Hash Algorithm — «безопасный алгоритм хеширования») и получает для каждого коммита свой уникальный хеш — результат 
	хеширования. Обычно хеш — это короткая (40 символов в случае SHA-1) строка, которая состоит из цифр 0—9 и латинских букв A—F 
	неважно, заглавных или строчных). Она обладает следующими важными свойствами:
	если хеш получить дважды для одного и того же набора входных данных, то результат будет гарантированно одинаковый;
	если хоть что-то в исходных данных поменяется (хотя бы один символ), то хеш тоже изменится (причём сильно).
	
	Хеш — основной идентификатор коммита
	Git хранит таблицу соответствий хеш → информация о коммите. Если вы знаете хеш, вы можете узнать всё остальное: автора и дату коммита 
	и содержимое закоммиченных файлов. Можно сказать, что хеш — основной идентификатор коммита.
	При работе с Git хеши будут встречаться вам регулярно. Их можно будет передавать в качестве параметра разным Git-командам, чтобы 
	указать, с каким коммитом нужно произвести то или иное действие.
	Все хеши и таблицу хеш → информация о коммите Git сохраняет в служебные файлы. Они находятся в скрытой папке .git в репозитории проекта.


Логирование файлов (log — "журнал (записей)")
	После вызова git log появляется список коммитов. Элементы, из которых состоит описание:
	- строка из цифр и латинских букв после слова commit — это хеш коммита;
	- Author — имя автора и его электронная почта;
	- Date — дата и время создания коммита;
	- в конце находится сообщение коммита.
	
	Получить сокращённый лог — git log --oneline
	Получить подробный лог с деревом коммитов — git log --graph
	
	
HEAD — всему голова	
	Файл HEAD (англ. «голова», «головной») — один из служебных файлов папки .git. 
	Он указывает на коммит, который сделан последним (то есть на самый новый).
	
	Внутри HEAD — ссылка на служебный файл: refs/heads/master (или refs/heads/main в зависимости от названия ветки). 
	Если заглянуть в этот файл, можно увидеть хеш последнего коммита.
	
	Если нужно передать последний коммит, то вместо его хеша можно просто написать слово HEAD — Git поймёт, 
	что вы имели в виду последний коммит.
	
	
Статусы файлов - untracked/tracked, staged и modified
	Одна из ключевых задач Git — отслеживать изменения файлов в репозитории. Для этого каждый файл помечается каким-либо статусом. 
	Рассмотрим основные:
	
	untracked (англ. «неотслеживаемый») 
	-  новые файлы в Git-репозитории помечаются как untracked, то есть неотслеживаемые. Git «видит», 
	что такой файл существует, но не следит за изменениями в нём. У untracked-файла нет предыдущих версий, зафиксированных в коммитах 
	или через команду git add.
	
	staged (англ. «подготовленный») 
	- после выполнения команды git add файл попадает в staging area(от англ. stage — «сцена», «этап(процесса)»
	и area — «область»), то есть в список файлов, которые войдут в коммит. В этот момент файл находится в состоянии staged.
	
	! Staging area, index и cache
	Staging area также называют index (англ. «каталог») или cache (англ. «кеш»), а состояние файла staged иногда называют indexed или cached.
	Все три варианта могут встречаться в документации и в качестве флагов команд Git. 
	А также в интернете — например, в вопросах и ответах на сайте Stack Overflow.
	
	tracked (англ. «отслеживаемый») 
	- состояние tracked — это противоположность untracked. Оно довольно широкое по смыслу: в него попадают файлы, которые уже были 
	зафиксированы с помощью git commit, а также файлы, которые были добавлены в staging area командой git add. То есть все файлы, в которых Git так или иначе отслеживает изменения.
	
	modified (англ. «изменённый») 
	- состояние modified означает, что Git сравнил содержимое файла с последней сохранённой версией и нашёл отличия. 
	Например, файл был закоммичен и после этого изменён.
	
	! Для файлов в состояниях staged и modified обычно не указывают, что они также tracked, потому что это состояние подразумевается.
	
	! Команда git add добавляет в staging area только текущее содержимое файла. Если вы, например, сделаете git add file.txt, а затем 
	измените file.txt, то новое содержимое файла не будет находиться в staging. Git сообщит об этом с помощью статуса modified: 
	файл изменён относительно той версии, которая уже в staging. Чтобы добавить в staging последнюю версию, нужно выполнить
	git add file.txt ещё раз.
	
	
Схема по статусам файлов в git (код mermaid  https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)

```mermaid
graph LR;
  untracked -- "git add" --> staged;
  staged    -- "git commit -m 'описание коммита' "     --> tracked/comitted;
  tracked/comitted  --> modified (внесли изменения в файл)  -- "git add" --> staged;

%% стрелка без текста для примера: 
  A --> B;
```

Какие состояния показывает git status
	Большинство файлов в типичном проекте будут находиться в состоянии tracked (то есть закоммичены и не изменены после коммита). 
	Вы не увидите это состояние в выводе команды git status — иначе она бы каждый раз выводила список вообще всех файлов проекта.
	В итоге git status показывает только следующие состояния файлов:
	- staged (Changes to be committed в выводе git status);
	- modified (Changes not staged for commit);
	- untracked (Untracked files).
	
	
Правила для сообщений в коммитах
	- сообщение коммита легко читается;
	- сообщение информативное;
	- все сообщения оформлены в одном стиле
	
	Есть различные стили (Conventional Commits)
	- корпоративный   https://www.conventionalcommits.org/ru/v1.0.0-beta.4/#спецификация
	- Git Hub стлиль