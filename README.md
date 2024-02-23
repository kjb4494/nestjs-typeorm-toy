# Nestjs TypeORM Toy Project

TypeORM과 실무를 익히기 위한 NestJs 공부용 토이 프로젝트

## Env

- Versions

  - node v20.11.0
  - npm 10.2.4
  - yarn 1.22.21
  - typescript 5.3.3

- VSCode Settings

  ```json
  {
    "workbench.colorTheme": "Default Dark+",
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
      "source.fixAll": "explicit"
    },
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
  ```

- Added eslintrc.js Settings

  ```js
  rules: {
  	<!-- [lf -> auto] Delete `␍` eslint (prettier/prettier) -->
  	'prettier/prettier': [
  		'error',
  		{
  			endOfLine: 'auto',
  		},
  	],
  	<!-- [error -> warn] 'A' is declared but its value is never read. ts(6133) -->
  	'@typescript-eslint/no-unused-vars': 'warn'
  }
  ```

- Added Modules

  - **nest-js/config**: `yarn add @nestjs/config`
  - **validation**: `yarn add class-validator class-transformer`
  - **[_joi_](https://github.com/hapijs/joi)**: `yarn add joi`
  - **typeorm + postgres**: `yarn add pg typeorm typeorm-naming-strategies @nestjs/typeorm`
  - **[_cookie-parser_](https://docs.nestjs.com/techniques/cookies)**: `yarn add cookie-parser`, `yarn add -D @types/cookie-parser`

- .env for local

  ```text
  # app
  NODE_ENV=development
  PORT=5000
  ADMIN_USER=...
  ADMIN_PASSWORD=...
  SECRET_KEY=...
  DB_USERNAME=...
  DB_PASSWORD=...
  DB_HOST=localhost
  DB_PORT=5433
  DB_NAME=...

  # db
  POSTGRES_DB=testdb
  POSTGRES_USER=testuser
  POSTGRES_PASSWORD=P@ssw0rd
  ```

- docker
  ```shell
  docker-compose up -d
  ```

## Installation

```bash
$ yarn install
```

## Running the app

```bash
# development
$ yarn run start

# watch mode
$ yarn run start:dev

# production mode
$ yarn run start:prod
```

## Test

```bash
# unit tests
$ yarn run test

# e2e tests
$ yarn run test:e2e

# test coverage
$ yarn run test:cov
```
