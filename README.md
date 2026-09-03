# 🚀 Forkop Domain List

Удобное управление списком доменов для **Forkop** через GitHub.

Репозиторий хранит основной список в файле `domain.txt`, а веб-панель позволяет добавлять, удалять и редактировать домены прямо с телефона или компьютера.

---

## ✨ Возможности

- ➕ быстрое добавление домена;
- 🗑️ удаление домена с автоматическим сохранением;
- ↩️ отмена последнего изменения;
- ✏️ редактирование домена прямо в списке;
- ☑️ выбор нескольких доменов и массовое удаление;
- 🔎 быстрый поиск;
- 📋 добавление сразу нескольких доменов;
- 🔄 синхронизация с GitHub;
- 📱 удобная мобильная версия;
- 🌐 доступ к списку через обычный `raw` URL.

---

## 📁 Структура

```text
forkop-list/
├── domain.txt     # основной список доменов
└── index.html     # веб-панель управления
```

### `domain.txt`

По одному домену на строку:

```text
youtube.com
googlevideo.com
ytimg.com
youtubei.googleapis.com
```

Без `http://`, `https://` и путей.

---

## 🌐 Raw-ссылка для Forkop

Основная ссылка на список:

```text
https://raw.githubusercontent.com/nektopandroid-source/forkop-list/main/domain.txt
```

Именно её можно использовать там, где Forkop умеет загружать удалённый список.

---

## 🖥️ Веб-панель

Панель доступна через GitHub Pages:

```text
https://nektopandroid-source.github.io/forkop-list/
```

Она работает и на компьютере, и на телефоне.

### Что можно делать

**Добавить**

Введите:

```text
example.com
```

и нажмите **Добавить**.

**Удалить**

Нажмите **Удалить** напротив домена.

Изменение автоматически записывается в GitHub.

**Изменить**

Нажмите **Изменить**, исправьте домен и подтвердите `✓`.

**Массовое удаление**

Выберите несколько строк и нажмите:

```text
Удалить выбранные
```

---

## 🔐 GitHub Token

Веб-панели нужен GitHub Fine-grained Personal Access Token.

Рекомендуемые параметры:

### Repository access

```text
Only select repositories
└── forkop-list
```

### Repository permissions

```text
Contents → Read and write
```

Другие разрешения не нужны.

> ⚠️ Никогда не публикуйте свой GitHub Token в репозитории, README, скриншотах или сообщениях.

Токен сохраняется локально в браузере панели.

---

## 🛠️ Установка GitHub Pages

1. Откройте **Settings** репозитория.
2. Перейдите в **Pages**.
3. В разделе **Build and deployment** выберите:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`
4. Нажмите **Save**.

После публикации:

```text
https://nektopandroid-source.github.io/forkop-list/
```

---

## 🧩 Chrome-расширение

Для быстрого добавления текущего сайта можно использовать отдельное Chrome-расширение.

Откройте сайт → нажмите значок расширения → **Добавить текущий сайт**.

Также доступно через контекстное меню:

```text
ПКМ → Добавить сайт в Forkop
```

Расширение автоматически:

1. определяет домен текущего сайта;
2. убирает `www.`;
3. проверяет наличие домена в списке;
4. добавляет его в `domain.txt`;
5. сохраняет изменения через GitHub API.

---

## 🔄 Как всё работает

```text
                ┌─────────────────┐
                │     Forkop      │
                └────────┬────────┘
                         │
                         │ GET
                         ▼
              domain.txt on GitHub
                         ▲
                         │
                  GitHub API
                         │
              ┌──────────┴──────────┐
              │                     │
       Web-панель                Chrome
       GitHub Pages             расширение
              │                     │
              └─────────┬───────────┘
                        │
                      Add/Edit/Delete
```

---

## 💡 Рекомендации

Храните в `domain.txt` только домены, например:

```text
youtube.com
googlevideo.com
ytimg.com
reddit.com
```

Не добавляйте:

```text
https://youtube.com/watch?v=123
www.youtube.com/
youtube.com/something
```

Панель автоматически нормализует ввод, но сам файл лучше держать чистым.

---

## 📌 Репозиторий

**GitHub:**

https://github.com/nektopandroid-source/forkop-list

**Raw list:**

https://raw.githubusercontent.com/nektopandroid-source/forkop-list/main/domain.txt

**Web panel:**

https://nektopandroid-source.github.io/forkop-list/

---

### ⭐ Forkop Domain List

> Простое редактирование списка доменов + GitHub + удобная мобильная панель.
