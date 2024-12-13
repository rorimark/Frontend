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