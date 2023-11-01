# trainingTS

1. Встановлюємо TS. npm install -g typescript // TS встановлюється глобально на комп. один раз
2. Створюємо файл типу test.ts
3. Компілюємо файл - tsc test.ts (З'являється файл test.js)
   Cтежити за зміною файлу в режимі реального часу, виконавши команду: tsc test.ts -w
4. Налаштовуємо компілятор (створення проекту TS) - якщо є багато файлів, щоб не компілювати їх окремо кожний
   4.1. створимо нову папку (наприклад, TS_Lessons), перейдемо до неї та виконаємо в консолі команду: tsc --init.
   4.2. створить файл tsconfig.json, який містить стандартні налаштування TypeScript.

{
"compilerOptions": {
"allowJs": false,
"allowSyntheticDefaultImports": true,
"emitDecoratorMetadata": true,
"esModuleInterop": true,
"experimentalDecorators": true,
"lib": ["ES2021"],
"module": "es2020",
"moduleResolution": "node",
"preserveConstEnums": true,
"skipLibCheck": true,
"strictNullChecks": true,
"target": "es2019"
},
"include": ["**/*.ts"]
}

5.  Створимо в проекті файл. index.html та index.ts
6.  встановимо сервер @web/dev-server. Але для початку ініціалізуємо проєкт через npm:
    npm init -y
    Тепер встановимо сам сервер:
    npm i --save-dev @web/dev-server
    Перейдемо до файлу package.json, де нам потрібно додати команду start:

             {
             "name": "courses_ts",
             "version": "1.0.0",
             "description": "",
             "scripts": {
                 "start": "web-dev-server --node-resolve --open --watch"
             },
             "keywords": [],
             "author": "",
             "license": "ISC",
             "devDependencies": {
                 "@web/dev-server": "^0.2.1"
             }
             }

    А тепер просто запускаємо:
    npm start
