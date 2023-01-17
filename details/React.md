# Фронтенд. React

### Дизайнер

Для дизайнеров используем Figma. [Инструкция](https://github.com/iu5git/Standards/blob/main/docs/Tutorial_MUI.pdf). При работе отрисовки макетов необходимо использовать [MUI For Figma](https://mui.com/store/items/figma-react/?utm_source=marketing&utm_medium=referral&utm_campaign=home-products)

### JavaScript
Для большинства библиотек желательно использовать последнюю мажорную версию, допускается 1 предыдущая мажорная версия. 

Не требуем соблюдение последних минорных и патч версий, просто советуем всегда обновляться, чтобы переход на новый мажор был проще. Если для библиотеки требования отличны от данных, то это будет упомянуто.

Для JS НЕОБХОДИМО наличие файлов `package.json` и `package-lock.json`. Используем только npm, никакого yarn

### Для работы JS необходимо наличие Node и npm

Node - желательно использовать LTS версию из списка, допускается предыдущая LTS версия https://github.com/nodejs/release#release-schedule
Npm - разрешено использовать только последнюю мажорную версию, которая поддерживается выбранной Node https://nodejs.org/ru/download/releases/

### Линтинг файлов
**Требуются инструкции. Отложено на второй этап**

Необходимо проводить статический анализ кода. Для этого будут использоваться следующие библиотеки: eslint, stylelint, prettier, lint-staged, husky
Browserlist - специальный формат описания поддерживаемых версий браузеров https://www.npmjs.com/package/browserslist
Eslint - линтинг js, ts кода https://www.npmjs.com/package/eslint
Stylelint - линтинг css кода  https://www.npmjs.com/package/stylelint
Prettier - форматирование кода  https://www.npmjs.com/package/prettier
Lint-staged - поиск измененных файлов в комете (используется для pre-commit хуков)  https://www.npmjs.com/package/lint-staged
Husky - разрешены только версии 4.x.x и 3.x.x, pre-commit хук https://www.npmjs.com/package/husky

### Фреймворк

Единственным разрешенным фреймворком является React https://www.npmjs.com/package/react. Можно использовать все библиотеки, которые находятся в официальных репозиториях React. 2 основных репозитория https://github.com/facebook/react/ https://github.com/facebook/create-react-app/tree/main/packages

### Менеджер состояний 

- Redux Toolkit

### UI-KIt

Единственным разрешенный Ui-Kit - MUI https://github.com/mui/material-ui. Посмотреть все компоненты можно тут https://mui.com/material-ui/getting-started/overview/ 

### Типизиция

Код должен быть написан на TypeScript https://www.npmjs.com/package/typescript . Нежелательно использования any, as, @ts-ignore в типизации. Мы типизируем код, чтобы помочь себе, а не потому что от нас требуют 

### Работа с Api

Вся работа с Api должна быть типизирована с помощью TypeScript, для генерации Api по Swagger необходимо использовать библиотеку swagger-typescript-api https://www.npmjs.com/package/swagger-typescript-api . Слой работы с Api должен быть отделен от остального приложения и не зависеть от него. Клиент для работы с бекендом axios https://www.npmjs.com/package/axios

### Логгирование ошибок

Для логгирования ошибок необходимо использовать библиотеку Sentry https://www.npmjs.com/package/@sentry/browser . При инициализации необходимо подключать библиотеки @sentry/react https://www.npmjs.com/package/@sentry/react и @sentry/tracing https://www.npmjs.com/package/@sentry/tracing

### Тестирование кода (unit)

Для тестирования кода Unit тестами необходимо использовать библиотеку Jest https://www.npmjs.com/package/jest . Рекомендуется полностью покрывать тестами слой Api, важные функции проекта. Тестирование Ui компонентов по желанию

### Тестирование кода (e2e)

E2e тесты - это достаточно сложно, поэтому пишем по желанию разработчиков. Для этого используем библиотеку playwright https://www.npmjs.com/package/playwright

### Метрики

Нужны ли нам метрики? Если хотим знать, сколько где было кликов и тд, рекомендуется для этого библиотека Яндекс.Метрика. Она легко настраивается и не требует сильных вложений

