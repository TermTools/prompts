# Laravel 12 + Breeze (Blade) Setup

## Steps

1. **Create project (lock to v12)**

```bash
composer create-project laravel/laravel:^12 my-laravel-app
cd my-laravel-app
```

2. **Quick DB setup (SQLite for local dev)**

```bash
php -r "file_exists('database') ?: mkdir('database');"
touch database/database.sqlite
php -r "\$env=file_get_contents('.env'); \$env=preg_replace('/^DB_CONNECTION=.*/m','DB_CONNECTION=sqlite',\$env); \$env=preg_replace('/^DB_HOST=.*/m','',\$env); \$env=preg_replace('/^DB_PORT=.*/m','',\$env); \$env=preg_replace('/^DB_DATABASE=.*/m','DB_DATABASE='.getcwd().'/database/database.sqlite',\$env); \$env=preg_replace('/^DB_USERNAME=.*/m','',\$env); \$env=preg_replace('/^DB_PASSWORD=.*/m','',\$env); file_put_contents('.env',\$env);"
```

*(Note: Users preferring MySQL can skip this and configure `.env` accordingly.)*

3. **Install Breeze (Blade)**

```bash
composer require laravel/breeze --dev
php artisan breeze:install
```

Select: Blade → No → PHPUnit

4. **Frontend deps & build**

```bash
npm install
npm run build
```

5. **App key + storage + migrate**

```bash
php artisan key:generate
php artisan storage:link
php artisan migrate
```

6. **Run tests**

```bash
php artisan test -q
```

7. **Serve locally**

```bash
php artisan serve
# Visit http://127.0.0.1:8000
```

8. **Verify auth**

* Open **/register** → create user
* Sign out, then **/login** → sign in
* Confirm redirect and authenticated UI

9. **Git init**

```bash
git init
git add .
git commit -m "chore: bootstrap Laravel 12 with Breeze (Blade) + SQLite"
```

## Deliverables Checklist

✓ Fresh Laravel 12 install (locked to v12)  
✓ Breeze (Blade) installed; auth scaffolding generated  
✓ Database configured (SQLite), migrations run  
✓ Frontend built (Vite)  
✓ Basic tests run  
✓ Verification checklist (register/login/logout)  
✓ First git commit