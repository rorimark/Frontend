Работа с **локальным хранилищем (localStorage)** и **сеансовым хранилищем (sessionStorage)** — важная часть веб-разработки. Это позволяет сохранять данные на стороне клиента.

---

## **1. Что такое localStorage и sessionStorage?**

### **localStorage**

- Позволяет сохранять данные в браузере **на постоянной основе**.
- Данные остаются даже после перезагрузки страницы или закрытия браузера.

### **sessionStorage**

- Сохраняет данные **на время текущей сессии**.
- Данные удаляются, как только пользователь закрывает вкладку или окно браузера.

---

## **2. Общие характеристики**

- Данные хранятся в формате **ключ-значение**.
- Доступно через объект `localStorage` или `sessionStorage`.
- Данные сохраняются только в строковом формате.

---

## **3. Основные методы**

### **Сохранение данных**

```javascript
localStorage.setItem('key', 'value'); // Для localStorage
sessionStorage.setItem('key', 'value'); // Для sessionStorage
```

### **Получение данных**

```javascript
const value = localStorage.getItem('key');
console.log(value); // 'value'
```

### **Удаление данных**

```javascript
localStorage.removeItem('key');
sessionStorage.removeItem('key');
```

### **Очистка хранилища**

Удаляет все данные из хранилища.

```javascript
localStorage.clear();
sessionStorage.clear();
```

### **Получение всех ключей**

Можно получить ключи, используя свойство `length` и метод `key()`.

```javascript
for (let i = 0; i < localStorage.length; i++) {
    const key = localStorage.key(i);
    console.log(key, localStorage.getItem(key));
}
```

---

## **4. Различия между localStorage и sessionStorage**

|Характеристика|localStorage|sessionStorage|
|---|---|---|
|Срок хранения|Постоянно|Только в рамках текущей сессии|
|Удаление данных|Вручную или программно|При закрытии вкладки|
|Доступ из других вкладок|Да|Нет|

---

## **5. Работа с объектами: сериализация и десериализация**

Так как хранилище работает только со строками, для хранения объектов их нужно преобразовать с помощью JSON.

### **Сохранение объектов (сериализация)**

Используйте `JSON.stringify()` для преобразования объекта в строку.

```javascript
const user = { name: 'Alice', age: 25 };

localStorage.setItem('user', JSON.stringify(user));
```

### **Получение объектов (десериализация)**

Используйте `JSON.parse()` для преобразования строки обратно в объект.

```javascript
const userData = localStorage.getItem('user');
const user = JSON.parse(userData);

console.log(user.name); // 'Alice'
console.log(user.age); // 25
```

---

## **6. Пример использования**

### **Сохранение и загрузка настроек пользователя**

```javascript
// Сохранение настроек
const settings = {
    theme: 'dark',
    notifications: true
};
localStorage.setItem('settings', JSON.stringify(settings));

// Загрузка настроек
const savedSettings = localStorage.getItem('settings');
if (savedSettings) {
    const settingsObj = JSON.parse(savedSettings);
    console.log(settingsObj.theme); // 'dark'
    console.log(settingsObj.notifications); // true
}
```

---

## **7. Ограничения localStorage и sessionStorage**

- **Объём хранилища:** ограничен примерно 5 МБ (в зависимости от браузера).
- **Данные доступны только в рамках домена:** данные, сохранённые на одном домене, недоступны на другом.
- **Нет защиты данных:** данные могут быть просмотрены через инструменты разработчика, поэтому не храните конфиденциальную информацию (например, пароли).

---

## **8. Использование событий**

Можно отслеживать изменения в хранилище с помощью события `storage`.

### **Пример: Слушатель изменений**

Этот слушатель срабатывает при изменении `localStorage` из другой вкладки.

```javascript
window.addEventListener('storage', (event) => {
    console.log('Ключ:', event.key);
    console.log('Новое значение:', event.newValue);
    console.log('Старое значение:', event.oldValue);
});
```

---

## **9. Лучшие практики**

### **1. Используйте JSON для сложных данных**

Для удобной работы с объектами всегда преобразуйте их с помощью `JSON.stringify()` и `JSON.parse()`.

### **2. Очистите данные, если они больше не нужны**

Не перегружайте хранилище ненужной информацией, особенно в `localStorage`.

### **3. Никогда не храните чувствительные данные**

Не храните пароли, токены или личную информацию. Для таких данных используйте безопасные способы хранения, такие как куки с флагом `HttpOnly`.

### **4. Проверяйте существование данных**

Перед использованием данных из хранилища проверяйте, существуют ли они:

```javascript
const data = localStorage.getItem('key');
if (data) {
    console.log('Данные существуют:', JSON.parse(data));
} else {
    console.log('Данных нет');
}
```

---

## **10. Дополнительные возможности**

### **1. Проверка доступности localStorage**

Некоторые браузеры могут блокировать использование хранилища (например, в приватном режиме).

```javascript
function isLocalStorageAvailable() {
    try {
        localStorage.setItem('test', 'test');
        localStorage.removeItem('test');
        return true;
    } catch (e) {
        return false;
    }
}
```

### **2. Удаление устаревших данных**

Добавляйте к данным информацию о времени их добавления и проверяйте её при загрузке:

```javascript
const saveDataWithExpiry = (key, value, ttl) => {
    const now = new Date();
    const item = {
        value: value,
        expiry: now.getTime() + ttl // Время жизни в миллисекундах
    };
    localStorage.setItem(key, JSON.stringify(item));
};

const getDataWithExpiry = (key) => {
    const itemStr = localStorage.getItem(key);
    if (!itemStr) return null;

    const item = JSON.parse(itemStr);
    const now = new Date();

    if (now.getTime() > item.expiry) {
        localStorage.removeItem(key);
        return null;
    }

    return item.value;
};

// Пример использования
saveDataWithExpiry('user', { name: 'Alice' }, 10000); // 10 секунд
console.log(getDataWithExpiry('user'));
```