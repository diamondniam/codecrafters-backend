# codecrafters-backend

## Установка

1. Склонируйте репозиторий:

    ```bash
    git clone https://github.com/Bivekich/codecrafters-backend.git
    cd codecrafters-backend
    ```

2. Установите зависимости:

    ```bash
    npm install
    ```

3. Создайте файл `.env` в корне проекта и добавьте следующие строки:

    ```plaintext
    PORT=<PORT>
    MONGODB_URI=<DB_URI>
    ```

## Описание файлов

- **server.js:** Основной файл сервера, где настраивается подключение к MongoDB и маршруты.
- **routes/heroes.js:** Файл маршрутов для работы с записями "Hero".

## Запуск сервера

Запустите сервер командой:

```bash
npm run dev
```

Сервер будет запущен на порту, указанном в файле .env (по умолчанию 3000).

## API Маршруты

### Получение записи Hero

- **URL:** `GET /hero`
- **Пример ответа:**

```json
[
  {
    "_id": "66516704a9ea1f2cde7ac340",
    "title": "CodeCrafters.",
    "description": "Lorem ipsum dore la forte plui la dore amet isun etre lore lorem. Vous parle espaniol quel amon avoir."
  }
]
```

### Обновление записи Hero

- **URL:** `PUT /hero/:id`
- **Тело запроса:**

```json
{
  "title": "CodeCrafters.",
  "description": "Lorem ipsum dore la forte plui la dore amet isun etre lore lorem. Vous parle espaniol quel amon avoir."
}
```

- **Пример ответа:**

```plaintext
Запись Hero с id 66516704a9ea1f2cde7ac340 успешно обновлена
```

## Лицензия

Этот проект лицензирован под MIT License.