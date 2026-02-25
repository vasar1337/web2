# vasar — TikTok Video Downloader

Минималистичный сервис для скачивания видео с TikTok без водяного знака.

## Технологии

- **Backend:** PHP 8+
- **Frontend:** Vue.js 3
- **Стили:** Tailwind CSS
- **Сервер:** XAMPP (Apache)

## Требования

- XAMPP с PHP 8.0 или выше
- Включенный модуль `curl` в PHP

## Установка

1. **Скопируйте проект в папку XAMPP:**
   ```
   c:\xampp\htdocs\vasar
   ```

2. **Включите cURL в PHP:**
   - Откройте `c:\xampp\php\php.ini`
   - Найдите строку `;extension=curl`
   - Уберите точку с запятой: `extension=curl`
   - Перезапустите Apache в XAMPP Control Panel

3. **Откройте в браузере:**
   ```
   http://localhost/vasar
   ```

## Использование

1. Откройте TikTok и скопируйте ссылку на видео
2. Вставьте ссылку в поле ввода на сайте
3. Нажмите кнопку "Скачать"
4. Выберите нужный формат и скачайте видео

## API

### POST /api/download

**Запрос:**
```json
{
    "url": "https://www.tiktok.com/@username/video/1234567890"
}
```

**Ответ:**
```json
{
    "success": true,
    "data": {
        "id": "1234567890",
        "title": "Название видео",
        "author": {
            "username": "username",
            "nickname": "Имя автора",
            "avatar": "https://..."
        },
        "video": {
            "no_watermark": "https://...",
            "watermark": "https://...",
            "music": "https://...",
            "cover": "https://..."
        },
        "stats": {
            "plays": 1000000,
            "likes": 50000,
            "comments": 1000,
            "shares": 500,
            "downloads": 200
        },
        "duration": 30,
        "created_at": 1234567890
    }
}
```

## Структура проекта

```
vasar/
├── app/
│   └── Http/
│       └── Controllers/
│           └── TikTokController.php
├── public/
│   ├── index.php
│   └── .htaccess
├── resources/
│   └── views/
│       └── welcome.php
├── routes/
│   └── web.php
├── config/
│   └── app.php
└── composer.json
```

## Особенности

- ✨ Минималистичный дизайн
- 🎨 Тёмная тема с градиентами
- 📱 Адаптивный интерфейс
- ⚡ Быстрая загрузка
- 🔒 Без регистрации
- 💰 Полностью бесплатно

## Лицензия

MIT License

---

**vasar** © 2026
