**DOM (Document Object Model)** — это программный интерфейс для работы с HTML и XML-документами. Он представляет документ в виде дерева объектов, которое JavaScript может использовать для изменения структуры, стилей и содержания страницы.

---

### 1. **Что такое DOM?**

- **DOM** — это объектная модель документа, которая позволяет взаимодействовать с HTML через JavaScript.
- Документ представляется в виде **дерева узлов (nodes)**, где каждый элемент HTML, текст, комментарий и атрибут — это отдельный узел.

Пример HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Пример DOM</title>
</head>
<body>
    <h1 id="title">Заголовок</h1>
    <p class="text">Текст абзаца.</p>
</body>
</html>
```

Пример DOM-структуры для этого HTML:

- html
    - head
        - title
    - body
        - h1
        - p

---

### 2. **Основные свойства DOM**

#### 2.1. **`document`**

Объект `document` представляет весь HTML-документ.

Примеры:

```javascript
console.log(document.title); // "Пример DOM"
console.log(document.body);  // <body>...</body>
```

#### 2.2. **Узлы (Nodes)**

DOM состоит из узлов, каждый из которых относится к одному из типов:

- **Элемент (element)** — теги HTML (`<div>`, `<h1>`, `<p>`).
- **Текст (text)** — текст внутри элементов.
- **Атрибуты (attributes)** — атрибуты HTML-тегов.
- **Комментарий (comment)** — комментарии в HTML.

---

### 3. **Доступ к элементам DOM**

#### 3.1. **По идентификатору (ID)**

```javascript
let title = document.getElementById("title");
console.log(title); // <h1 id="title">Заголовок</h1>
```

#### 3.2. **По классу**

```javascript
let paragraphs = document.getElementsByClassName("text");
console.log(paragraphs[0]); // <p class="text">Текст абзаца.</p>
```

#### 3.3. **По тегу**

```javascript
let headers = document.getElementsByTagName("h1");
console.log(headers[0]); // <h1 id="title">Заголовок</h1>
```

#### 3.4. **По CSS-селектору**

- `querySelector` возвращает первый элемент, соответствующий селектору.
- `querySelectorAll` возвращает все элементы, соответствующие селектору.

```javascript
let firstParagraph = document.querySelector(".text");
let allParagraphs = document.querySelectorAll("p");
```

---

### 4. **Манипуляции с DOM**

#### 4.1. **Изменение текста**

Свойство `textContent` меняет текст внутри элемента.

```javascript
let title = document.getElementById("title");
title.textContent = "Новый заголовок";
```

#### 4.2. **Изменение HTML внутри элемента**

Свойство `innerHTML` меняет HTML-содержимое элемента.

```javascript
let paragraph = document.querySelector(".text");
paragraph.innerHTML = "<strong>Обновленный текст</strong>";
```

#### 4.3. **Изменение атрибутов**

Используйте методы:

- `setAttribute` — для установки атрибута.
- `getAttribute` — для получения значения атрибута.
- `removeAttribute` — для удаления атрибута.

```javascript
let title = document.getElementById("title");
title.setAttribute("class", "highlight");
console.log(title.getAttribute("id")); // "title"
title.removeAttribute("id");
```

#### 4.4. **Изменение стилей**

Свойство `style` позволяет изменять CSS-стили элемента.

```javascript
let title = document.getElementById("title");
title.style.color = "blue";
title.style.fontSize = "24px";
```

---

### 5. **Создание, добавление и удаление элементов**

#### 5.1. **Создание элемента**

С помощью метода `createElement`:

```javascript
let newDiv = document.createElement("div");
newDiv.textContent = "Это новый элемент";
```

#### 5.2. **Добавление элемента в DOM**

С помощью `appendChild`:

```javascript
document.body.appendChild(newDiv);
```

С помощью `prepend` (в начало родителя):

```javascript
document.body.prepend(newDiv);
```

#### 5.3. **Удаление элемента**

Метод `remove`:

```javascript
let title = document.getElementById("title");
title.remove();
```

Метод `removeChild`:

```javascript
document.body.removeChild(newDiv);
```

---

### 6. **Перебор элементов DOM**

#### 6.1. Использование `for...of`

```javascript
let paragraphs = document.querySelectorAll("p");
for (let paragraph of paragraphs) {
    console.log(paragraph.textContent);
}
```

#### 6.2. Использование `forEach`

```javascript
paragraphs.forEach(paragraph => {
    console.log(paragraph.textContent);
});
```

---

### 7. **События и слушатели**

#### 7.1. Добавление обработчиков событий

С помощью метода `addEventListener`:

```javascript
let button = document.querySelector("button");
button.addEventListener("click", () => {
    alert("Кнопка нажата!");
});
```

#### 7.2. События мыши

- `click` — клик.
- `mouseover` — наведение курсора.
- `mouseout` — уход курсора.

#### 7.3. События клавиатуры

- `keydown` — нажатие клавиши.
- `keyup` — отпускание клавиши.

Пример:

```javascript
document.addEventListener("keydown", event => {
    console.log(`Нажата клавиша: ${event.key}`);
});
```

---

### 8. **Навигация по DOM**

#### 8.1. Родительский элемент

```javascript
let parent = document.querySelector(".text").parentNode;
```

#### 8.2. Дочерние элементы

```javascript
let children = document.body.children;
```

#### 8.3. Следующий/предыдущий элемент

```javascript
let next = document.querySelector(".text").nextElementSibling;
let previous = document.querySelector(".text").previousElementSibling;
```

---

### 9. **Делегирование событий**

Делегирование позволяет обработать события для группы элементов через общего родителя:

```javascript
document.body.addEventListener("click", event => {
    if (event.target.tagName === "BUTTON") {
        console.log("Клик по кнопке!");
    }
});
```

---

### 10. **Практические советы**

1. **Минимизируйте использование `innerHTML`**: он может быть небезопасным (опасность XSS-атак).
2. **Добавляйте события через `addEventListener`**, а не через атрибуты `onclick` в HTML.
3. Используйте **`querySelector`** и **`querySelectorAll`** для гибкого поиска элементов.

---

### Резюме

1. **DOM** — это интерфейс для работы с HTML-документами.
2. Используйте методы для доступа к элементам: `getElementById`, `querySelector`, `querySelectorAll`.
3. Манипулируйте содержимым через `textContent`, `innerHTML`, и атрибутами через `setAttribute`.
4. Добавляйте и удаляйте элементы с помощью `appendChild`, `remove`.
5. Работайте с событиями с помощью `addEventListener`.
6. Используйте делегирование событий для оптимизации.