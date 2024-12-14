___
### **Базовые концепции JavaScript**

#### 1. [Введение](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%91%D0%B0%D0%B7%D0%BE%D0%B2%D1%8B%D0%B5%20%D0%BA%D0%BE%D0%BD%D1%86%D0%B5%D0%BF%D1%86%D0%B8%D0%B8%20JavaScript)

- Что такое JavaScript и его назначение.
- Подключение JS к HTML (через `<script>`).
- Взаимодействие с консолью (`console.log()`).

#### 2. Основы синтаксиса

- [Переменные](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9F%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5%20%D0%B2%20JavaScript): `var`, `let`, `const`.
- [Типы данных](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A2%D0%B8%D0%BF%D1%8B%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B2%20JavaScript): `number`, `string`, `boolean`, `undefined`, `null`, `object`, `symbol`, `bigint`.
- Операторы:
    - [Арифметические](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%90%D1%80%D0%B8%D1%84%D0%BC%D0%B5%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B5%20%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B%20%D0%B2%20JavaScript) (`+`, `-`, `*`, `/`, `%`).
    - [Сравнения](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9E%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B%20%D1%81%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F%20%D0%B2%20JavaScript) (`===`, `!==`, `<`, `>`, `<=`, `>=`).
    - [Логические](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9B%D0%BE%D0%B3%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B5%20%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B%20%D0%B2%20JavaScript) (`&&`, `||`, `!`).
- [Шаблонные строки (template literals)](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5%20%D1%81%D1%82%D1%80%D0%BE%D0%BA%D0%B8%20(Template%20Literals)%20%D0%B2%20JavaScript): `` `Hello, ${name}!` ``.

#### 3. Управляющие структуры

- [Условные операторы](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A3%D1%81%D0%BB%D0%BE%D0%B2%D0%BD%D1%8B%D0%B5%20%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B%20%D0%B2%20JavaScript): `if`, `else if`, `else`, тернарный оператор.
- [Циклы](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A6%D0%B8%D0%BA%D0%BB%D1%8B%20%D0%B2%20JavaScript):
    - `for`.
    - `while` и `do...while`.
    - `for...of` и `for...in`.

#### 4. [Функции](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A4%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B8%20%D0%B2%20JavaScript)

- Объявление функций:
    - Функции с именем (`function name()`).
    - Анонимные функции.
    - Стрелочные функции (`=>`).
- Параметры и аргументы.
- Возврат значений (`return`).

#### 5. [Массивы](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9C%D0%B0%D1%81%D1%81%D0%B8%D0%B2%D1%8B%20%D0%B2%20JavaScript)

- Создание массивов.
- Основные методы:
    - Добавление/удаление элементов (`push`, `pop`, `shift`, `unshift`).
    - Обход массива (`forEach`, `map`, `filter`, `reduce`).
    - Поиск элементов (`find`, `findIndex`, `includes`).
    - Сортировка (`sort`, `reverse`).
- Деструктуризация массивов.

#### 6. [Объекты](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9E%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D1%8B%20%D0%B2%20JavaScript)

- Создание объектов.
- Доступ к свойствам (`obj.key`, `obj['key']`).
- Добавление/удаление свойств.
- Перебор объектов (`for...in`, `Object.keys`, `Object.values`, `Object.entries`).
- Деструктуризация объектов.

#### 7. [DOM (Document Object Model)](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2FDocument%20Object%20Model%20(DOM)%20%D0%B2%20JavaScript)

- Поиск элементов:
    - `document.querySelector`.
    - `document.getElementById`.
- Изменение элементов:
    - `textContent`, `innerHTML`, `style`.
    - Добавление/удаление классов (`classList.add`, `classList.remove`).
- Создание и удаление элементов:
    - `document.createElement`.
    - `appendChild`, `removeChild`.

#### 8. [События](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A1%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D1%8F%20%D0%B2%20JavaScript)

- Добавление обработчиков событий:
    - `addEventListener`.
    - Атрибуты событий в HTML (`onclick`, `onchange`).
- Типы событий: `click`, `input`, `submit`, `keydown`, `mousemove`.
- Объект события: `event`.

---

### **Средний уровень JavaScript**

#### 9. [Модули](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9C%D0%BE%D0%B4%D1%83%D0%BB%D0%B8%20%D0%B2%20JavaScript)

- Импорт и экспорт (`import`, `export`).
- Работа с модулями через `<script type="module">`.

#### 10. [Работа с API](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20API%20%D0%B2%20JavaScript)

- Fetch API:
    - Отправка GET и POST запросов.
    - Обработка ответов (`response.json()`).
- Асинхронность:
    - Обещания (Promises): `then`, `catch`, `finally`.
    - `async/await`.

#### 11. [Локальное хранилище](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%BC%20%D1%85%D1%80%D0%B0%D0%BD%D0%B8%D0%BB%D0%B8%D1%89%D0%B5%D0%BC%20%D0%B2%20JavaScript)

- `localStorage` и `sessionStorage`.
- JSON: сериализация (`JSON.stringify`) и десериализация (`JSON.parse`).

#### 12. [Ошибки и отладка](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%BE%D1%88%D0%B8%D0%B1%D0%BA%D0%B0%D0%BC%D0%B8%20%D0%B8%20%D0%BE%D1%82%D0%BB%D0%B0%D0%B4%D0%BA%D0%B0%20%D0%B2%20JavaScript)

- Блоки `try...catch`.
- Пользовательские ошибки (`throw`).
- Отладка в DevTools браузера.

#### 13. [Date и Time](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%B4%D0%B0%D1%82%D0%BE%D0%B9%20%D0%B8%20%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%B5%D0%BC%20%D0%B2%20JavaScript)

- Объект `Date`.
- Получение текущего времени.
- Форматирование дат.

#### 14. [Регулярные выражения](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%A0%D0%B5%D0%B3%D1%83%D0%BB%D1%8F%D1%80%D0%BD%D1%8B%D0%B5%20%D0%B2%D1%8B%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%20(Regular%20Expressions%20%D0%B8%D0%BB%D0%B8%20RegEx)%20%D0%B2%20JavaScript)

- Основы синтаксиса регулярных выражений.
- Методы: `test`, `match`, `replace`.

#### 15. [Классы и ООП](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%9A%D0%BB%D0%B0%D1%81%D1%81%D1%8B%20%D0%B8%20%D0%9E%D0%9E%D0%9F%20%D0%B2%20JavaScript)

- Создание классов (`class`).
- Конструкторы (`constructor`).
- Методы класса.
- Наследование (`extends`, `super`).

---

### **Продвинутый уровень JavaScript**

#### 16. [Асинхронное программирование](obsidian://open?vault=Frontend-Development-Learning-Roadmap&file=%D0%9E%D0%B1%D1%83%D1%87%D0%B0%D1%8E%D1%89%D0%B8%D0%B5%20%D0%BC%D0%B0%D1%82%D0%B5%D1%80%D0%B8%D0%B0%D0%BB%D1%8B%2FJS%2F%D0%90%D1%81%D0%B8%D0%BD%D1%85%D1%80%D0%BE%D0%BD%D0%BD%D0%BE%D0%B5%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B2%20JavaScript)

- Таймеры: `setTimeout`, `setInterval`.
- Event Loop и стек вызовов.
- Работа с генераторами (`function*`).

#### 17. Продвинутая работа с объектами

- `Object.create`, прототипы.
- Методы объектов:
    - `Object.assign`.
    - `Object.freeze`.
    - `Object.seal`.

#### 18. Продвинутая работа с массивами

- Методы:
    - `flat`, `flatMap`.
    - `reduceRight`.
- Копирование массивов:
    - Глубокое и поверхностное копирование.

#### 19. Symbol и итераторы

- Использование символов (`Symbol`).
- Создание итераторов и генераторов.

#### 20. Map, Set, WeakMap, WeakSet

- Разница между коллекциями.
- Использование `Map` и `Set` для хранения данных.

#### 21. Продвинутая работа с событиями

- Деликатные события: `debounce` и `throttle`.
- События на фазе всплытия и захвата (event bubbling, capturing).
- Делегирование событий.

#### 22. Web Workers

- Основы многопоточности в JS.
- Создание и использование воркеров.

#### 23. Canvas и WebGL

- Основы рисования на `<canvas>`.
- Создание простых анимаций.

---

### **Инструменты и экосистема**

- Работа с NPM (Node Package Manager).
- Основы Webpack, Vite или Parcel.
- Линтеры (ESLint) и форматтеры (Prettier).

---

### **Практические навыки**

- Разработка приложений (например, To-Do List, калькулятор, чат).
- Участие в Open Source проектах.
- Решение задач на алгоритмы и структуры данных (Codewars, LeetCode).