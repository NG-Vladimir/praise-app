# Команда прославления — Mini App

Мини-приложение для Telegram. Хостится на GitHub Pages.

## Деплой (один раз)

1. На GitHub создайте **новый репозиторий**: [Create a new repository](https://github.com/new)  
   - Имя: **praise-app** (или любое другое)  
   - Public, без README.

2. В терминале выполните из **корня проекта** (папка `w`, не `gh-pages`):

```bash
cd /Users/vladimir/Desktop/w/gh-pages
git init
git add index.html README.md
git commit -m "Mini app: команда прославления"
git branch -M main
git remote add origin https://github.com/NG-Vladimir/praise-app.git
git push -u origin main
```

3. На GitHub: **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → Save.

4. Через 1–2 минуты приложение будет доступно по адресу:

   **https://NG-Vladimir.github.io/praise-app/**

5. В проекте в файле `.env` укажите (в корне папки `w`):

   ```
   MINI_APP_URL=https://NG-Vladimir.github.io/praise-app/
   ```

6. Перезапустите бота. Кнопка «Открыть мини-приложение» будет вести сразу в приложение, без промежуточных страниц.

## Обновление приложения

После изменений в `mini_app/index.html` скопируйте файл сюда и запушьте:

```bash
cp /Users/vladimir/Desktop/w/mini_app/index.html /Users/vladimir/Desktop/w/gh-pages/index.html
cd /Users/vladimir/Desktop/w/gh-pages
git add index.html
git commit -m "Update mini app"
git push
```
