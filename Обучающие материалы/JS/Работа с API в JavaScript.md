Работа с API — одна из важнейших тем в JavaScript, особенно в веб-разработке. Она позволяет отправлять запросы к удалённым серверам, получать данные и взаимодействовать с ними.

---

## **1. Что такое API?**

- **API (Application Programming Interface)** — это интерфейс, который позволяет приложениям взаимодействовать друг с другом.
- Например, веб-приложение может отправить запрос на сервер для получения данных (например, погоды, новостей или профиля пользователя).

### **REST API**

- Один из самых популярных типов API.
- Использует HTTP-методы:
    - `GET` — для получения данных,
    - `POST` — для отправки данных,
    - `PUT/PATCH` — для обновления данных,
    - `DELETE` — для удаления данных.

---

## **2. Fetch API**

**Fetch API** — это встроенный в браузеры способ отправки HTTP-запросов. Он работает асинхронно и возвращает **Promise**.

### **Основной синтаксис Fetch API**

```javascript
fetch(url, options)
    .then(response => {
        // Обработка ответа
    })
    .catch(error => {
        // Обработка ошибки
    });
```

---

### **Пример: Отправка GET-запроса**

```javascript
fetch('https://jsonplaceholder.typicode.com/posts')
    .then(response => {
        if (!response.ok) {
            throw new Error(`Ошибка: ${response.status}`);
        }
        return response.json(); // Преобразование ответа в JSON
    })
    .then(data => {
        console.log(data); // Вывод данных в консоль
    })
    .catch(error => {
        console.error('Ошибка запроса:', error);
    });
```

---

### **Передача параметров и опций**

Для более сложных запросов можно указать дополнительные параметры в объекте `options`:

- **Метод запроса** (`method`).
- **Тело запроса** (`body`).
- **Заголовки** (`headers`).

```javascript
fetch('https://jsonplaceholder.typicode.com/posts', {
    method: 'POST', // Тип запроса
    headers: {
        'Content-Type': 'application/json', // Указываем тип данных
    },
    body: JSON.stringify({
        title: 'Новая статья',
        body: 'Это текст статьи.',
        userId: 1
    })
})
    .then(response => response.json())
    .then(data => {
        console.log('Успешно создано:', data);
    })
    .catch(error => {
        console.error('Ошибка:', error);
    });
```

---

### **Методы Fetch API**

|Метод|Назначение|
|---|---|
|`fetch()`|Отправка HTTP-запросов.|
|`response.json()`|Преобразует ответ в JSON.|
|`response.text()`|Преобразует ответ в текст.|
|`response.blob()`|Преобразует ответ в двоичный объект (например, изображение).|
|`response.ok`|Возвращает `true`, если статус успешный.|
|`response.status`|Возвращает статус-код ответа (например, 200 или 404).|

---

### **Асинхронность с `async/await`**

Асинхронная функция позволяет писать асинхронный код в более "синхронном" стиле.

#### **Пример: Асинхронный GET-запрос**

```javascript
async function fetchPosts() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/posts');
        if (!response.ok) {
            throw new Error(`Ошибка: ${response.status}`);
        }
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.error('Ошибка запроса:', error);
    }
}

fetchPosts();
```

---

#### **Пример: Асинхронный POST-запрос**

```javascript
async function createPost() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/posts', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                title: 'Новая статья',
                body: 'Текст статьи',
                userId: 1
            })
        });
        const data = await response.json();
        console.log('Создано:', data);
    } catch (error) {
        console.error('Ошибка:', error);
    }
}

createPost();
```

---

## **3. Асинхронность в JavaScript**

Асинхронность позволяет выполнять долгие операции (например, запросы к серверу) без блокировки основного потока.

### **Основные понятия**

- **Promise** — объект, представляющий результат асинхронной операции.
- **async/await** — удобный синтаксис для работы с `Promise`.
- **Callback** — старый подход для работы с асинхронным кодом.

---

## **4. Обработка ошибок**

Обрабатывать ошибки важно, чтобы приложение не "падало" при сбое запроса.

### **С помощью `try/catch`**

```javascript
async function fetchData() {
    try {
        const response = await fetch('https://api.example.com/data');
        if (!response.ok) {
            throw new Error(`Ошибка: ${response.status}`);
        }
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.error('Произошла ошибка:', error);
    }
}
```

---

## **5. Параллельные запросы**

Для одновременного выполнения нескольких запросов можно использовать `Promise.all`.

```javascript
async function fetchMultiple() {
    try {
        const [users, posts] = await Promise.all([
            fetch('https://jsonplaceholder.typicode.com/users').then(res => res.json()),
            fetch('https://jsonplaceholder.typicode.com/posts').then(res => res.json())
        ]);
        console.log('Пользователи:', users);
        console.log('Посты:', posts);
    } catch (error) {
        console.error('Ошибка:', error);
    }
}

fetchMultiple();
```

---

## **6. Полезные утилиты**

### **Отмена запроса**

Fetch API не поддерживает отмену запросов "из коробки", но можно использовать `AbortController`.

```javascript
const controller = new AbortController();
const signal = controller.signal;

fetch('https://jsonplaceholder.typicode.com/posts', { signal })
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(err => {
        if (err.name === 'AbortError') {
            console.log('Запрос был отменён');
        } else {
            console.error('Ошибка:', err);
        }
    });

// Отмена запроса
controller.abort();
```

---

## **7. Заголовки и авторизация**

Если API требует авторизации, используйте заголовки.

#### **Пример: Bearer Token**

```javascript
fetch('https://api.example.com/secure-data', {
    method: 'GET',
    headers: {
        'Authorization': 'Bearer YOUR_ACCESS_TOKEN',
    }
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Ошибка:', error));
```

---

## **8. CORS (Cross-Origin Resource Sharing)**

Если вы получаете ошибку CORS, это значит, что сервер не разрешает запросы с вашего домена. Это проблема сервера, и её нельзя решить со стороны клиента. Вы можете:

- Использовать прокси-сервер.
- Настроить сервер, чтобы он разрешал ваш домен.

---

## **9. Полезные советы**

- Используйте **async/await** для упрощения чтения кода.
- Обрабатывайте ошибки (с помощью `try/catch`).
- Проверяйте статус ответа (`response.ok`, `response.status`).
- Документируйте работу с API (например, описывайте эндпоинты, заголовки, параметры).