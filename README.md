# Галерея митця — як запустити на Netlify

## 1. Опублікувати сайт
1. Створіть репозиторій на GitHub і завантажте туди всі ці файли.
2. На netlify.com: **Add new site → Import an existing project → GitHub** → оберіть репозиторій.
   Build command — порожньо, Publish directory — `.`
3. Сайт буде доступний за адресою `назва.netlify.app` (можна змінити в Site settings).

## 2. Увімкнути адмін-панель (тільки для митця)
1. У файлі `admin/config.yml` замініть `ВАШ_ЛОГІН/НАЗВА_РЕПОЗИТОРІЮ` на свої.
2. На GitHub: Settings → Developer settings → OAuth Apps → New OAuth App.
   - Homepage URL: адреса вашого сайту
   - Callback URL: `https://api.netlify.com/auth/done`
3. У Netlify: **Site configuration → Access & security → OAuth → Install provider → GitHub**,
   вставте Client ID та Client Secret.
4. Відкрийте `ваш-сайт.netlify.app/admin` і увійдіть через GitHub.

Додавати та редагувати зможе лише той, хто має доступ до репозиторію (тобто митець).
Для всіх інших адмінка просто не пустить.

## 3. Додавання картин
В адмін-панелі: **Картини (галерея) → Додати картину** → завантажте файл,
вкажіть назву й опис → **Publish**. Через ~1 хвилину картина на сайті.
Оригінальний файл зберігається без стиснення, тож 4K-якість у повному перегляді зберігається.

## Без адмінки (простіший варіант)
Покласти фото в `images/` і вручну додати запис у `data/paintings.json`.
