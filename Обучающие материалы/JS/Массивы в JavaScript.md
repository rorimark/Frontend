Массивы — это упорядоченные коллекции данных, которые могут содержать элементы любого типа (числа, строки, объекты, другие массивы и т.д.). Они используются для хранения списков и работы с ними.

---

### 1. **Создание массивов**

1. **С помощью литерала массива:**

```javascript
let fruits = ["яблоко", "банан", "вишня"];
```

2. **С помощью конструктора `Array`:**

```javascript
let fruits = new Array("яблоко", "банан", "вишня");
```

3. **Пустой массив:**

```javascript
let emptyArray = [];
```

4. **Массив с заданной длиной:**

```javascript
let arrayWithLength = new Array(5); // Создаёт массив длиной 5
```

---

### 2. **Обращение к элементам массива**

Элементы массива индексируются с 0:

```javascript
let fruits = ["яблоко", "банан", "вишня"];
console.log(fruits[0]); // "яблоко"
console.log(fruits[2]); // "вишня"
```

Изменение элемента:

```javascript
fruits[1] = "груша";
console.log(fruits); // ["яблоко", "груша", "вишня"]
```

---

### 3. **Основные свойства массива**

1. **`length`** — возвращает количество элементов:

```javascript
let fruits = ["яблоко", "банан", "вишня"];
console.log(fruits.length); // 3
```

2. Массивы могут содержать элементы разных типов:

```javascript
let mixed = [1, "текст", true, { key: "value" }];
```

---

### 4. **Основные методы массивов**

#### Добавление и удаление элементов:

1. **`push`** — добавляет элемент в конец массива.

```javascript
let fruits = ["яблоко"];
fruits.push("банан");
console.log(fruits); // ["яблоко", "банан"]
```

2. **`pop`** — удаляет последний элемент и возвращает его.

```javascript
let fruits = ["яблоко", "банан"];
let lastFruit = fruits.pop();
console.log(lastFruit); // "банан"
console.log(fruits); // ["яблоко"]
```

3. **`unshift`** — добавляет элемент в начало массива.

```javascript
let fruits = ["банан"];
fruits.unshift("яблоко");
console.log(fruits); // ["яблоко", "банан"]
```

4. **`shift`** — удаляет первый элемент и возвращает его.

```javascript
let fruits = ["яблоко", "банан"];
let firstFruit = fruits.shift();
console.log(firstFruit); // "яблоко"
console.log(fruits); // ["банан"]
```

---

#### Поиск и работа с элементами:

1. **`indexOf`** — возвращает индекс первого найденного элемента.

```javascript
let fruits = ["яблоко", "банан", "вишня"];
console.log(fruits.indexOf("банан")); // 1
```

2. **`includes`** — проверяет, содержит ли массив элемент.

```javascript
let fruits = ["яблоко", "банан"];
console.log(fruits.includes("вишня")); // false
```

---

#### Сортировка и изменение порядка:

1. **`reverse`** — меняет порядок элементов на обратный.

```javascript
let numbers = [1, 2, 3];
numbers.reverse();
console.log(numbers); // [3, 2, 1]
```

2. **`sort`** — сортирует элементы массива (по умолчанию как строки).

```javascript
let fruits = ["банан", "яблоко", "вишня"];
fruits.sort();
console.log(fruits); // ["банан", "вишня", "яблоко"]

let numbers = [10, 2, 3];
numbers.sort((a, b) => a - b); // Сортировка чисел по возрастанию
console.log(numbers); // [2, 3, 10]
```

---

#### Преобразование массива:

1. **`join`** — объединяет элементы массива в строку.

```javascript
let fruits = ["яблоко", "банан", "вишня"];
console.log(fruits.join(", ")); // "яблоко, банан, вишня"
```

2. **`split`** — разделяет строку на массив (используется на строках).

```javascript
let str = "яблоко, банан, вишня";
let fruits = str.split(", ");
console.log(fruits); // ["яблоко", "банан", "вишня"]
```

---

#### Изменение массива:

1. **`splice`** — добавляет, удаляет или заменяет элементы.

```javascript
let fruits = ["яблоко", "банан", "вишня"];
fruits.splice(1, 1, "груша"); // Удаляет 1 элемент с индекса 1 и добавляет "груша"
console.log(fruits); // ["яблоко", "груша", "вишня"]
```

2. **`slice`** — возвращает новый массив с выбранными элементами.

```javascript
let fruits = ["яблоко", "банан", "вишня"];
let slicedFruits = fruits.slice(0, 2); // С индекса 0 до 2 (не включая 2)
console.log(slicedFruits); // ["яблоко", "банан"]
```

---

#### Итерация по массиву:

1. **`forEach`** — выполняет функцию для каждого элемента.

```javascript
let fruits = ["яблоко", "банан", "вишня"];
fruits.forEach((fruit) => console.log(fruit));
// "яблоко"
// "банан"
// "вишня"
```

2. **`map`** — возвращает новый массив, преобразовав каждый элемент.

```javascript
let numbers = [1, 2, 3];
let squared = numbers.map((num) => num ** 2);
console.log(squared); // [1, 4, 9]
```

3. **`filter`** — возвращает новый массив с элементами, прошедшими проверку.

```javascript
let numbers = [1, 2, 3, 4];
let evenNumbers = numbers.filter((num) => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

4. **`reduce`** — сводит массив к одному значению.

```javascript
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // 10
```

---

### 5. **Деструктуризация массива**

Деструктуризация позволяет извлекать элементы массива в переменные.

#### Пример:

```javascript
let fruits = ["яблоко", "банан", "вишня"];
let [first, second] = fruits;
console.log(first); // "яблоко"
console.log(second); // "банан"
```

#### Деструктуризация с остаточными элементами:

```javascript
let fruits = ["яблоко", "банан", "вишня"];
let [first, ...rest] = fruits;
console.log(first); // "яблоко"
console.log(rest); // ["банан", "вишня"]
```

#### Пропуск элементов:

```javascript
let fruits = ["яблоко", "банан", "вишня"];
let [, , third] = fruits;
console.log(third); // "вишня"
```

---

### 6. **Работа с многомерными массивами**

Массивы могут содержать другие массивы.

Пример:

```javascript
let matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
];
console.log(matrix[1][2]); // 6
```

---

### 7. **Копирование массива**

1. **С помощью `slice`:**

```javascript
let numbers = [1, 2, 3];
let copy = numbers.slice();
```

2. **С помощью оператора разворота (`...`):**

```javascript
let numbers = [1, 2, 3];
let copy = [...numbers];
```

⚠️ Прямое присваивание создаёт ссылку, а не копию:

```javascript
let original = [1, 2, 3];
let copy = original;
copy[0] = 99;
console.log(original); // [99, 2, 3]
```

---

### Резюме

1. Массивы — это упорядоченные коллекции данных.
2. Основные методы:
    - **Добавление/удаление**: `push`, `pop`, `unshift`, `shift`.
    - **Изменение**: `splice`, `slice`.
    - **Итерация**: `forEach`, `map`, `filter`, `reduce`.
3. Деструктуризация позволяет удобно извлекать значения.
4. Используйте копирование (`slice`, `...`) для избежания изменения оригинального массива.