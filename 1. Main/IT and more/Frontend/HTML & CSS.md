## <span style="color:#e4522b">HTML</span>

`<video src=""></video>` - специальный тег, для добавления видео на страницу. У него есть атрибуты: `controls` - добавляет элементы контроля видео(кнопка пауза, стрелки, ползунок и т.д), `autoplay` - авто воспроизведение видео, не воспроизводится бесконечно, `muted` - убирает звук, `loop` - делает видео бесконечным, то есть оно постоянно воспроизводится и не останавливается. 

---

`<form action=''>Text</form>` - форма регистрации, обёртка для тегов `<label></label>` и `<input>`.

---

## <span style="color:#2f69f1">CSS</span>

`tranform: rotate(1turn);` - поворот на 360°. [Источник](https://www.freecodecamp.org/news/how-to-build-a-delightful-loading-screen-in-5-minutes-847991da509f)

---

`pointer-events: none;` - убирает возможность кликабелности элемента.

---

`class:active {
`transform: scale(.98);`
`}` - если наложено на элемент, то при клике на элемент он слегка уменьшается.

---

`::-webkit-scrollbar` - контролирует стили скроллбара браузера.
```css
::-webkit-scrollbar {
  width: 0;
}
```

Чтобы убрать scrollbar в Firefox нужно внутри звёздочки прописать `scrollbar-width: none;`.
Вот как это должно выглядеть:
```css
*{
 scrollbar-width: none;
}
```

---

Свойство `height` не анимируется. Вместо этого используй `max-height`. Его уже можно анимировать.

`resize: vertical` - свойство, которое запрещает менять размеры элемента. Значение `vertical` означает, что размер можно изменять только по вертикали. Чатсо применяется к тегу `<textarea></textarea>`.

---

При анимации псевдоэлементов `::before` или `::after` не должно быть пробелов при обращении к ним.  Пример:
`preview__button: hover.preview__button::before {}`, то есть `class:hover.class::before {}`. Также если есть текст, то нужно обернуть его в `span` и добавить `positionv: relative;`, чтобы он отображался поверх псевдоэлементов.

---

`overflow-x: hidden` - скрывает контент, который больше блока по горизонтали.

---

`minmax()` - функция для указания минимального и максимального размера элемента.

---
<br>

### display: grid;

#### Создание
`grid-template-columns` - свойство для создания колонок и их размера. Размер можно указывать в любой единице, но удобнее делать через фракции fractions(fr). ^c830ce
```css
.grid__container {
	grid-template-columns: 200px 200px; /* Две колонки по 200px. Если указать ещё значения, то количество колонок увеличится. */
}
```

`repeat(количество, размер)` - функция для повторяющихся размеров.

```css
.grid__container {
	grid-template-columns:repeat(3, 1fr); /* Три колонки по одной фракции/части/дроби */
}
```

Можно указывать несколько размеров: 
```css
.grid__container {
	grid-template-columns:repeat(10, 1fr, 2fr); /* Десять колонок. У нечётных размер будет в одну фракцию, а у чётных две фракции.  */
}

.grid__container_2 {
	grid-template-columns:repeat(10, 100px, 200px); /* Десять колонок. У нечётных размер будет в 100px, а у чётных 200px.  */
}
```
<br>

`grid-template-rows` - свойство для создания строк и их размера.  ^a12bc6

```css
.grid__container {
grid-template-rows:100px 200px 300px; /* Три строки. У первой размер 100px, у второй 200px, а у третьей 300px.  */
}

.grid__container_2 {
grid-template-columns:repeat(10, 200px, 300px); /* Десять cтрок. У нечётных размер будет в 200px, а у чётных 300px.  */
}
```
<br>

`grid-template` - свойство для создания строк и колонок, а также указания их размера - сокращение для [[#^a12bc6|grid-template-rows]] и [[#^c830ce|grid-template-columns]]:
```css
.grid-container {
	display:grid;
	grid-template: 50% 50% / 200px; /* "grid-template-rows / grid-template-columns" grid-сетка с двумя строками по 50% каждая и одним столбцом шириной 200 пикселей.*/
}
```

`grid-auto-rows` - задаёт размер для строк, для которых он явно не задан.
#### Позиционирование

`grid-column-gap` - свойство для указания отсупов между колонками. ^9ed7df

`grid-column-start` - указывает с какой колонки начинается элемент.
`grid-column-end` - указывает на какой колонке заканчивается элемент. ^576243

`grid-column` - свойство для определния начала и конца элемента через `/` - короткая запись для [[#^576243|grid-column-start и grid-column-end]]: ^b3df41

```css
.grid__container {
	display:grid;
	grid-column: 1/3; /* С какой колонки начинается / на какой колонку заканчивается. В данном случае с первой колонки по третью - элемент растяентся на три колонки. */
}
```
`justify-content` - такое же как и у *flex*.
`align-content` - выравнивание по оси Y.
`align-items` - в случае с *grid*, `align-items` выравнивает контент относительно ячейки по оси Y.
`justify-items` - делает то же самое, что и `align-items`, но по оси X.
<br>

`grid-row-gap` - свойство для указания отсупов между строками. ^779528

`grid-row-start` - указывает с какой строки начинается элемент.
`grid-row-end` - указывает на какой строке заканчивается элемент. ^d70817

`grid-row` - свойство для определения начала и конца строки через `/` -  короткая запись для [[#^d70817|grid-row-start и grid-row-end]]. ^ff4886

```css
.grid__container {
	display:grid;
	grid-row: 1/3; /* С какой строки начинается / на какой строке заканчивается. В данном случае с первой строки по третью - элемент растяентся на три строки. */
}
```

`grid-gap/gap` - короткая запись для [[#^779528|grid-row-gap]] и [[#^9ed7df|grid-column-gap]].

`grid-template-areas` - свойство для ручного позиционирования элементов на *grid* сетке:
```css
.container {
	display:grid;
	grid-template-areas:
					"header header"
					"sidebar content"
	gap: 10px;
	grid-template-columns: 150px 1fr;
	grid-template-rows: 50px 1fr
}
.header {
	grid-area: header;
}
.sidebar {
	grid-area: sidebar;
}
.content {
	grid-area: content;
}

```
Результат↓:
![[Pasted image 20251025172810.png]]

`grid-area` - свойство чтобы сразу указать начало и конец строк вместе с колонками - сокращение для [[#^ff4886|grid-row]] и [[#^b3df41|grid-column]]:
```css
.container{
	grid-area: 1/1/3/6; /* grid-row-start(1)/ grid-column-start(1), grid-row-end(3) и grid-column-end(6).*/
}
```


---
<br>

### Медиазапросы
```css
@media (max-width 1200px)
@media (max-width 998px)
@media (max-width 768px)
@media (max-width 576px)
@media (max-width 320px)
```
---
<br>