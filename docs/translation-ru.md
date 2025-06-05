# Как добавить новый перевод?

Предположим, что вы хотите добавить перевод с кодом `new`.

1. Скопируйте `app/locales/en.ts` в `app/locales/new.ts`.
2. Отредактируйте `new.ts`: замените `const en: LocaleType =` на `const new: PartialLocaleType` и в конце используйте `export default new;`.
3. Откройте `app/locales/index.ts`.
4. Добавьте строку `import new from './new.ts'`.
5. Включите `new` в список `ALL_LANGS`.
6. Добавьте `new: "new lang"` в `ALL_LANG_OPTIONS`.
7. Переведите строки в `new.ts`.
8. Создайте pull request, после чего автор его смержит.
