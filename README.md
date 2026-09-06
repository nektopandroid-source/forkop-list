# Forkop — список доменов

Небольшая веб-панель для управления `domain.txt` — списком доменов для Forkop.

## Возможности

- ➕ Добавление домена
- 📋 Массовое добавление
- 🔎 Поиск
- ☑️ Выбор доменов
- 🗑️ Удаление одного или нескольких доменов
- ♻️ Удаление дубликатов и нормализация
- 🔤 Сортировка
- ☁️ Синхронизация с GitHub
- 📱 Удобный ввод на телефоне

## Репозиторий

```text
nektopandroid-source/forkop-list
```

Ветка: `main`

Основной файл:

```text
domain.txt
```

Один домен на строку:

```text
youtube.com
googlevideo.com
example.com
```

Панель автоматически убирает `http://`, `https://`, `www.`, пути, пробелы и дубликаты.

## GitHub Token

Для записи в репозиторий нужен **Fine-grained Personal Access Token**.

Необходимое разрешение:

```text
Contents → Read and write
```

Желательно ограничить Token только репозиторием:

```text
nektopandroid-source/forkop-list
```

Token хранится только локально в браузере и не записывается в репозиторий.

## Синхронизация

После добавления или удаления панель сохраняет изменения через GitHub API и заново загружает `domain.txt`, поэтому список в интерфейсе обновляется после сохранения.

Для обновления используется принудительное обращение к GitHub API без браузерного кэша.

## GitHub Pages

`index.html` — обычная статическая страница. Её можно разместить через GitHub Pages.

Структура:

```text
forkop-list/
├── index.html
├── domain.txt
└── README.md
```

## URL списка

```text
https://raw.githubusercontent.com/nektopandroid-source/forkop-list/main/domain.txt
```

## Версия

**Forkop Domain Manager v14**

В v14:
- исправлено отображение галочек;
- убрана кнопка «Изменить»;
- сохранён удобный мобильный ввод.
