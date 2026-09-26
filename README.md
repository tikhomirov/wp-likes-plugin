# WordPress Simple Post Likes (`wp-likes-plugin`)

![WordPress Plugin](https://img.shields.io/badge/WordPress-5.0%2B-blue.svg)
![PHP Support](https://img.shields.io/badge/PHP-7.4%20%7C%208.0%20%7C%208.1%20%7C%208.2%20%7C%208.3-777BB4.svg)
![License](https://img.shields.io/badge/License-GPLv2-green.svg)

Простой и быстрый плагин лайков для записей и страниц WordPress с поддержкой AJAX, тем рейтингов и защиты от повторного голосования через IP/Cookie.

---

## 🚀 Возможности

- 👍 **Лайки без регистрации:** Быстрое голосование гостей и пользователей без перезагрузки страницы (AJAX).
- 🎨 **Кастомные темы оформления:** Встроенная поддержка стилей (FontAwesome, Bootstrap Stars, Bar Rating).
- 🔒 **Защита от накрутки:** Ограничение повторных лайков через Cookie и IP-адреса.
- 📊 **Метаданные:** Лайки хранятся в `postmeta` (ключ `_post_likes`), что позволяет легко сортировать популярные посты.

---

## 📥 Установка

### Через Composer (рекомендуется)
```bash
composer require tikhomirov/wp-likes-plugin
```

### Вручную
1. Скачайте ZIP-архив репозитория.
2. Распакуйте в директорию `/wp-content/plugins/wp-likes-plugin/`.
3. Активируйте плагин в админ-панели **Плагины → Установленные**.

---

## 💻 Использование

### Использование в цикле (The Loop)
```php
<?php
if (function_exists('get_simple_likes_button')) {
    echo get_simple_likes_button(get_the_ID());
}
// Или через шорткод:
echo do_shortcode('[like]');
?>
```

---

## 🛠️ Требования

- **WordPress:** 5.0 или выше
- **PHP:** 7.4, 8.0, 8.1, 8.2, 8.3
