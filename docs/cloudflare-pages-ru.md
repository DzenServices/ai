# Руководство по развёртыванию на Cloudflare Pages

## Создание нового проекта

Форкните репозиторий на GitHub, затем войдите на https://dash.cloudflare.com и перейдите в раздел Pages.

1. Нажмите «Create a project».
2. Выберите «Connect to Git».
3. Подключите Cloudflare Pages к своему аккаунту GitHub.
4. Выберите форкнутый проект.
5. Нажмите «Begin setup».
6. В полях «Project name» и «Production branch» оставьте значения по умолчанию или измените их при необходимости.
7. В разделе «Build Settings» выберите «Framework presets» → «Next.js».
8. Не используйте стандартную команду сборки из-за бага node:buffer. Вместо неё выполните:
   ```
   npx @cloudflare/next-on-pages --experimental-minify
   ```
9. Для «Build output directory» оставьте значение по умолчанию.
10. «Root Directory» менять не нужно.
11. В разделе «Environment variables» раскройте меню и нажмите «Add variable». Укажите следующие переменные:

    - `NODE_VERSION=20.1`
    - `NEXT_TELEMETRY_DISABLE=1`
    - `OPENAI_API_KEY=ваш_API_ключ`
    - `YARN_VERSION=1.22.19`
    - `PHP_VERSION=7.4`

    При необходимости добавьте:

    - `CODE= необязательно, пароли доступа, несколько значений разделяйте запятыми`
    - `OPENAI_ORG_ID= необязательно, ID организации в OpenAI`
    - `HIDE_USER_API_KEY=1 необязательно, запрет ввода API ключа пользователями`
    - `DISABLE_GPT4=1 необязательно, запрет использования GPT-4`
    - `ENABLE_BALANCE_QUERY=1 необязательно, разрешить запрос баланса`
    - `DISABLE_FAST_LINK=1 необязательно, отключить загрузку настроек из URL`
    - `OPENAI_SB=1 необязательно, использовать сторонний API OpenAI-SB`

12. Нажмите «Save and Deploy».
13. Отмените развёртывание («Cancel deployment»), так как нужно заполнить Compatibility flags.
14. Перейдите в «Build settings» → «Functions» и найдите «Compatibility flags».
15. Укажите `nodejs_compat` для «Configure Production compatibility flag» и «Configure Preview compatibility flag».
16. Зайдите в «Deployments» и нажмите «Retry deployment».
17. Готово.
