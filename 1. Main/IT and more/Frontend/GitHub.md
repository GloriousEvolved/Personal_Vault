Все команды выполняются в терминале. 

### Смена терминала в VS Code

1. Открыть VSCode.
2. Открыть терминал "Ctrl + `".
3. В открывшемся терминале нажать на стрелочку вниз рядом с плюсиком 
4. [![введите сюда описание изображения](https://i.sstatic.net/ITqkH.png)](https://i.sstatic.net/ITqkH.png)
5. Затем выбрать пункт "Select Default Profile"
6. В открывшемся сверху окошке выбираем желаемый терминал
7. 
8. [![введите сюда описание изображения](https://i.sstatic.net/TLedH.png)](https://i.sstatic.net/TLedH.png)

### Команды:

`Git add.` - добавляет все файлы. ^ebfbe6

`git add. Имя файла` - добавляет конкретный файл.

`Git branch()` - создание ветки

`git config user.name "Имя пользователя"` - команда для того, чтобы понять кто вводит изменения. ^9a9a84

`git commit -m 'Сообщение момента сохранениея'` - создаёт commit, сохранение файлов к которому можно вернуться. ^1a8ae9

`git config user.email "электронная почта пользователя"` - электронная почта, которая. ^70c9f2

`git clone ссылка` - клонирует репозиторий с Github ^8b6fd0

`Git checkout()` - 

`git init` - команда для инициализации репозитория. Превращает папку или файлы в Git репозиторий ^a64421

`Git status` - проверяет статус репозитория.

`git remote add origin ссылка` - привязывает папку или файлы к репозиторию на Github. ^fb1aea


`Git merge()` - слияние всех веток 

`git push -u origin 'название ветки'` - загружает папки в репозиторий на Github. ^4382b6

### Как загрузить проект на Github

Для того чтобы загрузить проект на Github нужны следующие команды: [[#^a64421|git init]] , [[#^ebfbe6|git add .]] , [[#^1a8ae9|git commit]] , [[#^fb1aea|git remote add origin]] , [[#^4382b6|git push]] . Если пользуешься Github впервые, то перед `git commit` нужно дополнительно прописать [[#^9a9a84|git config user.name]] и [[#^70c9f2|git config user.email]] . 

> [!info] Ошибка с нехваткой прав
>  Если выходит ошибка о том, что не хватает прав, нужно в поиске Windows зайти в "Диспетчер учётных данных" → `Учётные данные Windows` и в поле `Общие учётные данные` удалить учётку git. 
 
### Как удалить файл или папку на Github

Удалить файлы можно на самом сайте Github, выбрав нужные файл или папку, затем нажать на три точки слева сверху и кнопку <span style='color: #F85149;'>Delete directory</span>, если это папка или <span style='color: #F85149;'>Delete file</span> если это файл. После нажать на кнопку <span style='color: #4493F8;'>Load diff</span> и нажать на кнопку слева сверху <span style='background-color: #29903b; color: #fff; border-radius: 6px; padding: 0 12px'>Commit changes...</span>

Загрузить проект с Github себе на компьютер можно с помощью команды [[#^8b6fd0|git clone]]. Ссылка брать из кнопки <span style='background-color: #29903b; color: #fff; border-radius: 6px; padding: 3 10px;'><svg style='transform: translateY(10%); margin: 0 3px;' aria-hidden="true" focusable="false" class="hide-sm" viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="display: inline-block; user-select: none; vertical-align: text-bottom; overflow: visible;"><path d="m11.28 3.22 4.25 4.25a.75.75 0 0 1 0 1.06l-4.25 4.25a.749.749 0 0 1-1.275-.326.749.749 0 0 1 .215-.734L13.94 8l-3.72-3.72a.749.749 0 0 1 .326-1.275.749.749 0 0 1 .734.215Zm-6.56 0a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042L2.06 8l3.72 3.72a.749.749 0 0 1-.326 1.275.749.749 0 0 1-.734-.215L.47 8.53a.75.75 0 0 1 0-1.06Z"></path></svg> Code <svg style='transform: translateY(10%);' aria-hidden="true" focusable="false" class="octicon octicon-triangle-down" viewBox="0 0 16 16" width="16" height="16" fill="currentColor" style="display: inline-block; user-select: none; vertical-align: text-bottom; overflow: visible;"><path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path></svg></span>

