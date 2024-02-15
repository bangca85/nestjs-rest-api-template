
## Description

This is project Restfull API support for Levi leveler.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Project Structure

1. **Project Root Directory** : This is the top-level directory of your project. It will contain configuration files, node modules, and other top-level files like `README.md`, `package.json`, etc.
2. **Source Directory (`src/`)** : This directory will contain the main codebase of your application.

* **Modules (`src/modules/`)** : NestJS is module-driven, and each module represents a feature or a closely related set of features.
  *  **Example Module (`src/modules/example/`)** : This could be a user module, product module, etc. Each module should be self-contained.
  * `example.controller.ts`: Handles HTTP requests and responses.
  * `example.service.ts`: Contains business logic.
  * `example.module.ts`: Groups together the controllers and services.
  * `example.entity.ts`: (If using ORM) Represents the database model.
  * `dto/`: Data transfer objects folder for defining the shape of data for various operations like create, update, etc.
* **Common or Shared (`src/common/` or `src/shared/`)** : For reusable code across modules.
  * `constants/`: Constants used throughout the application.
  * `decorators/`: Custom decorators like `@CurrentUser()`.
  * `filters/`: Exception filters for handling errors.
  * `guards/`: Guards for routes like `AuthGuard`.
  * `middlewares/`: Middlewares like logging or request validation.
  * `pipes/`: Custom pipes for validation or transformation.
  * `interceptors/`: Interceptors for logging, transforming responses, etc.
* **Configuration (`src/config/`)** : For application configuration.
  * `configuration.ts`: Centralized configuration settings.
* **Authentication (`src/auth/`)** : For authentication logic.
  * `auth.module.ts`
  * `auth.service.ts`
  * `strategies/`: Passport strategies like JWT, local, etc.
* **Database (`src/database/`)** : If using an ORM like TypeORM.
  * `database.module.ts`: Database module configuration.
  * `database.providers.ts`: Database connection providers.
* **Main file (`src/main.ts`)** : The entry point of the application.

1. **Environment Files (`/`)** : Root level `.env` files for storing configuration that changes between environments.
2. **Test Directory (`test/`)** : For your tests. Structure it similarly to your `src/` directory.
3. **Miscellaneous Directories** :

* **Logs (`logs/`)** : If you're logging to files, store them here.
* **Scripts (`scripts/`)** : For custom utility scripts like database seeding, etc.
* **Public (`public/`)** : For static files served directly by the server.

1. **Documentation (`docs/`)** : For project documentation.
2. **Docker Files** : If using Docker, include your `Dockerfile` and `docker-compose.yml` at the root.

This structure is scalable and follows the principle of separation of concerns, making it easier to manage as your application grows. Remember, the exact structure can vary based on your specific requirements and preferences.

## License

Nest is [MIT licensed](LICENSE).

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest
