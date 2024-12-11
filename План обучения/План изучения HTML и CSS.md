Вот подробный список тем, которые нужно изучить в HTML и CSS, организованных шаг за шагом от основ до продвинутого уровня. Этот список покрывает все ключевые аспекты, необходимые для профессиональной работы фронтенд-разработчиком.

---

### **HTML**

#### 1. Введение

- Что такое HTML и его роль в веб-разработке.
- Основная структура HTML-документа:
    
    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>Document</title>
      </head>
      <body>
      </body>
    </html>
    ```
    
- Теги: что это такое и как их использовать.

#### 2. Базовые теги

- `<html>`, `<head>`, `<body>`.
- `<title>`, `<meta>` (основные атрибуты, такие как charset, viewport).
- `<h1>`–`<h6>` (заголовки).
- `<p>` (абзацы), `<br>` (разрыв строки), `<hr>` (горизонтальная линия).

#### 3. Семантические теги

- `<header>`, `<footer>`, `<main>`, `<section>`, `<article>`, `<aside>`.
- `<nav>` (навигация).
- `<figure>`, `<figcaption>`, `<time>`.

#### 4. Работа с текстом

- Форматирование текста:
    - `<strong>`, `<em>`, `<b>`, `<i>`.
    - `<mark>`, `<small>`, `<sup>`, `<sub>`, `<u>`.
- Списки:
    - Нумерованные (`<ol>`), ненумерованные (`<ul>`), вложенные списки.
    - Элементы списка (`<li>`).
- Ссылки:
    - `<a>` (атрибуты `href`, `target`, `rel`).

#### 5. Работа с изображениями и мультимедиа

- `<img>`:
    - Атрибуты `src`, `alt`, `width`, `height`.
- Мультимедиа:
    - `<video>` и атрибуты `controls`, `autoplay`, `loop`.
    - `<audio>` и атрибуты `controls`, `autoplay`.

#### 6. Формы

- Теги форм:
    - `<form>` и атрибуты `action`, `method`.
    - `<input>` (типы: `text`, `password`, `email`, `number`, `radio`, `checkbox`, `file`, `submit`, `reset`, `button`, и т.д.).
    - `<textarea>`.
    - `<select>` и `<option>`.
    - `<label>` (атрибут `for`).
- Валидация форм:
    - Атрибуты: `required`, `pattern`, `min`, `max`, `maxlength`, `minlength`.

#### 7. Таблицы

- `<table>`, `<tr>`, `<th>`, `<td>`, `<caption>`.
- Объединение ячеек: `rowspan`, `colspan`.

#### 8. Элементы управления

- `<button>` (атрибуты `type`, `disabled`).
- `<details>`, `<summary>`.
- `<progress>`, `<meter>`.

#### 9. Графика и анимация

- `<canvas>`: основы рисования на Canvas.
- SVG (основные элементы: `<svg>`, `<circle>`, `<rect>`, `<line>`, `<path>`).

#### 10. Прогрессивные темы HTML

- Метаданные: `<meta>` для SEO и Open Graph.
- Микроразметка (Schema.org).
- ARIA-атрибуты для доступности.
- Использование `<iframe>`.

---

### **CSS**

#### 1. Основы

- Что такое CSS и его роль в веб-разработке.
- Подключение CSS:
    - Внешние файлы (`<link>`).
    - Встроенный CSS (`<style>`).
    - Инлайн-стили.

#### 2. Селекторы

- Базовые селекторы: `*`, `tag`, `.class`, `#id`.
- Группировка и комбинации:
    - Группы (`h1, h2`).
    - Родитель/потомок (`div p`).
    - Прямой потомок (`div > p`).
    - Соседние элементы (`+`, `~`).
- Псевдоклассы:
    - Стандартные (`:hover`, `:focus`, `:visited`, `:first-child`, `:nth-child()`).
- Псевдоэлементы (`::before`, `::after`).

#### 3. Основы стилизации

- Цвета:
    - Именованные, HEX, RGB, HSL.
    - Прозрачность (RGBA).
- Единицы измерения:
    - Абсолютные (`px`, `cm`).
    - Относительные (`%`, `em`, `rem`, `vh`, `vw`).
- Шрифты:
    - Свойства: `font-family`, `font-size`, `font-style`, `font-weight`.
    - Подключение шрифтов (Google Fonts, @font-face).
- Прочее:
    - `line-height`, `text-align`, `text-transform`, `letter-spacing`.

#### 4. Модель блока (Box Model)

- Отступы:
    - `margin`, `padding`.
- Границы:
    - `border`, `border-radius`.
- Размеры:
    - `width`, `height`, `max-width`, `min-height`.

#### 5. Расположение элементов

- Display:
    - Типы: `block`, `inline`, `inline-block`, `none`.
    - Современные свойства: `grid`, `flex`.
- Позиционирование:
    - `static`, `relative`, `absolute`, `fixed`, `sticky`.
    - `z-index`.
- Overflow: `visible`, `hidden`, `scroll`, `auto`.

#### 6. Flexbox

- Основные свойства:
    - `display: flex`, `flex-direction`, `justify-content`, `align-items`.
- Расширенные свойства:
    - `align-content`, `flex-wrap`, `flex-grow`, `flex-shrink`, `flex-basis`.

#### 7. Grid Layout

- Основные свойства:
    - `display: grid`, `grid-template-rows`, `grid-template-columns`.
    - `grid-gap`, `justify-items`, `align-items`.
- Расширенные возможности:
    - `grid-template-areas`, `grid-auto-flow`.

#### 8. Адаптивность

- Media Queries:
    - Использование: `@media`.
    - Примеры: `max-width`, `min-width`, `orientation`.
- Адаптивные единицы (`vw`, `vh`, `%`).

#### 9. Анимации и переходы

- Переходы:
    - `transition` (время, свойства, функции сглаживания).
- Анимации:
    - `@keyframes`.
    - Свойство `animation` (имя, длительность, задержка, повторение).

#### 10. Продвинутые темы CSS

- CSS-переменные:
    - Объявление (`--variable`) и использование (`var(--variable)`).
- CSS Grid + Flexbox (совместное использование).
- Анимации с CSS: использование библиотеки (например, Animate.css).

#### 11. Препроцессоры

- SASS/SCSS:
    - Переменные.
    - Вложенность.
    - Миксины.
    - Наследование.

#### 12. Оптимизация и организация CSS

- Организация файловой структуры (BEM, ITCSS).
- Минификация CSS.
- Инструменты (PostCSS, Autoprefixer).