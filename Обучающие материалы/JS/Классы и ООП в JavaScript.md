## **1. Основы ООП**

Объектно-ориентированное программирование (ООП) — это парадигма программирования, в которой основными концепциями являются **объекты** и **классы**.

### **Ключевые принципы ООП**

1. **Инкапсуляция** — объединение данных и методов, которые работают с этими данными, в один объект.
2. **Наследование** — способность одного класса наследовать свойства и методы другого класса.
3. **Полиморфизм** — использование единого интерфейса для работы с разными типами данных.
4. **Абстракция** — скрытие деталей реализации и предоставление только необходимых функций.

---

## **2. Классы в JavaScript**

### **Что такое класс?**

Класс — это шаблон для создания объектов с определёнными свойствами и методами.

### **Создание класса**

В JavaScript классы создаются с использованием ключевого слова `class`:

```javascript
class Person {
    constructor(name, age) {
        this.name = name; // Свойство объекта
        this.age = age;   // Свойство объекта
    }

    // Метод класса
    sayHello() {
        console.log(`Привет, меня зовут ${this.name}, мне ${this.age} лет.`);
    }
}

// Создание объекта на основе класса
const person1 = new Person('Алексей', 25);
person1.sayHello(); // Привет, меня зовут Алексей, мне 25 лет.
```

---

## **3. Конструктор**

### **Метод `constructor`**

Метод `constructor` вызывается при создании нового объекта и используется для инициализации свойств.

```javascript
class Car {
    constructor(brand, model) {
        this.brand = brand;
        this.model = model;
    }

    getInfo() {
        return `${this.brand} ${this.model}`;
    }
}

const car1 = new Car('Toyota', 'Corolla');
console.log(car1.getInfo()); // Toyota Corolla
```

---

## **4. Методы**

Методы — это функции, определённые внутри класса.

### **Пример метода:**

```javascript
class Calculator {
    add(a, b) {
        return a + b;
    }

    multiply(a, b) {
        return a * b;
    }
}

const calc = new Calculator();
console.log(calc.add(5, 3));       // 8
console.log(calc.multiply(5, 3)); // 15
```

---

## **5. Свойства**

Свойства задаются в конструкторе. Также в ES6+ можно использовать **свойства класса** (не зависящие от экземпляров):

```javascript
class Rectangle {
    width = 0; // Свойство класса
    height = 0; // Свойство класса

    constructor(width, height) {
        this.width = width;
        this.height = height;
    }

    getArea() {
        return this.width * this.height;
    }
}

const rect = new Rectangle(5, 10);
console.log(rect.getArea()); // 50
```

---

## **6. Инкапсуляция**

Инкапсуляция позволяет скрывать детали реализации и предоставлять интерфейс для работы с объектом.  
Для приватных полей используется символ `#`.

```javascript
class BankAccount {
    #balance = 0; // Приватное поле

    deposit(amount) {
        this.#balance += amount;
    }

    getBalance() {
        return this.#balance;
    }
}

const account = new BankAccount();
account.deposit(100);
console.log(account.getBalance()); // 100
// account.#balance = 100; // Ошибка: невозможно получить доступ к приватному полю
```

---

## **7. Наследование**

### **Что такое наследование?**

Наследование позволяет одному классу (дочернему) получать свойства и методы другого класса (родительского).

### **Создание дочернего класса**

Ключевое слово `extends` используется для указания родительского класса.

```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }

    speak() {
        console.log(`${this.name} издаёт звук.`);
    }
}

class Dog extends Animal {
    speak() {
        console.log(`${this.name} лает.`);
    }
}

const dog = new Dog('Бобик');
dog.speak(); // Бобик лает.
```

---

## **8. Полиморфизм**

Полиморфизм позволяет дочерним классам изменять поведение методов родительского класса.

```javascript
class Shape {
    getArea() {
        throw new Error('Метод getArea должен быть переопределён');
    }
}

class Circle extends Shape {
    constructor(radius) {
        super();
        this.radius = radius;
    }

    getArea() {
        return Math.PI * this.radius ** 2;
    }
}

class Square extends Shape {
    constructor(side) {
        super();
        this.side = side;
    }

    getArea() {
        return this.side ** 2;
    }
}

const shapes = [new Circle(5), new Square(4)];

shapes.forEach(shape => {
    console.log(shape.getArea());
});
// 78.53981633974483 (площадь круга)
// 16 (площадь квадрата)
```

---

## **9. Статические методы и свойства**

### **Статические методы**

Методы, доступные только на уровне класса, а не объекта.

```javascript
class MathUtils {
    static add(a, b) {
        return a + b;
    }
}

console.log(MathUtils.add(5, 3)); // 8
```

### **Статические свойства**

Свойства, доступные только на уровне класса.

```javascript
class Config {
    static appName = 'MyApp';
}

console.log(Config.appName); // MyApp
```

---

## **10. Абстракция**

Абстракция достигается за счёт разделения общего интерфейса и конкретной реализации. В JavaScript используются базовые классы (через наследование) для этого.

---

## **11. Работа с `this`**

`this` в методах класса указывает на текущий экземпляр объекта.

```javascript
class Counter {
    constructor() {
        this.count = 0;
    }

    increment() {
        this.count++;
    }
}

const counter = new Counter();
counter.increment();
console.log(counter.count); // 1
```

---

## **12. Прототипы и классы**

Классы — это "сахар" над прототипами, которые исторически использовались для создания объектов и наследования.

```javascript
function Person(name) {
    this.name = name;
}

Person.prototype.sayHello = function () {
    console.log(`Привет, меня зовут ${this.name}.`);
};

const person = new Person('Иван');
person.sayHello(); // Привет, меня зовут Иван.
```

---

## **13. Лучшие практики**

1. Используйте классы для организации кода и инкапсуляции.
2. Не злоупотребляйте приватными полями, если это не нужно.
3. Пишите читаемый и простой код: наследуйте только там, где это оправдано.
4. Используйте современные фичи ES6+: `static`, `#`, наследование.