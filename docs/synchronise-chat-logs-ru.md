# Синхронизация истории чатов с UpStash

## Необходимые условия
- учётная запись GitHub
- собственный сервер ChatGPT-Next-Web
- [UpStash](https://upstash.com)

## Первые шаги
1. Зарегистрируйтесь в UpStash.
2. Создайте базу данных.

    ![Регистрация и вход](./images/upstash-1.png)

    ![Создание базы](./images/upstash-2.png)

    ![Выбор сервера](./images/upstash-3.png)

3. Найдите раздел REST API и скопируйте `UPSTASH_REDIS_REST_URL` и `UPSTASH_REDIS_REST_TOKEN` (⚠Не делитесь токеном!⚠)

   ![Копирование](./images/upstash-4.png)

4. Вставьте `UPSTASH_REDIS_REST_URL` и `UPSTASH_REDIS_REST_TOKEN` в настройки синхронизации и нажмите **Check Availability**.

    ![Синхронизация 1](./images/upstash-5.png)

    Если всё настроено правильно, увидите сообщение об успешной проверке.

    ![Проверка завершена](./images/upstash-6.png)

5. Готово!

   ![Отличная работа](./images/upstash-7.png)
