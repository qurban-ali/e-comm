# e-comm

A Laravel 8 application with authenticated dashboards, category management routes and role-specific routes using Laratrust.

## Local development

This is a legacy Laravel 8 project. Use a PHP and Node.js environment compatible with the locked dependencies; review dependency security before deploying publicly.

```bash
git clone https://github.com/qurban-ali/e-comm.git
cd e-comm
composer install
cp .env.example .env
php artisan key:generate
npm ci
npm run dev
```

Create an empty local MySQL database, then set `DB_DATABASE`, `DB_USERNAME` and `DB_PASSWORD` in `.env`. With the local database configured, run:

```bash
php artisan migrate
php artisan serve
```

Open the local URL printed by Artisan (usually http://127.0.0.1:8000). Run `npm run watch` to rebuild frontend assets during development, and `php artisan test` to run tests against a dedicated test database. Never use production credentials for local development or testing.

