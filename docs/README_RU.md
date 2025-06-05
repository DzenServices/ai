# Документация на русском языке

## Запуск приложения локально

1. Установите Node.js версии 18 или новее и Yarn.
2. Создайте файл `.env.local` в корне проекта и добавьте в него ваш ключ API:
   ```
   OPENAI_API_KEY=sk-xxxx
   # при необходимости можно задать BASE_URL для прокси
   ```
3. Установите зависимости и запустите приложение:
   ```bash
   yarn install
   yarn dev
   ```

## Запуск в Docker

```bash
docker pull yidadaa/chatgpt-next-web

docker run -d -p 3000:3000 \
   -e OPENAI_API_KEY=sk-xxxx \
   -e CODE=your-password \
   yidadaa/chatgpt-next-web
```

## Дополнительные материалы

Больше информации можно найти в других файлах каталога `docs`.
