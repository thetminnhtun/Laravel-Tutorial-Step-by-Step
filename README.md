## Running the Laravel-Tutorial-Step-by-Step
### First

1. `composer install` in project folder

2. create the database (and database user if necessary) and add them to the `.env` file or run command `cp .env.example .env` (only Linux and Mac)

```
DB_DATABASE=your_db_name
DB_USERNAME=your_db_user
DB_PASSWORD=your_password
```

3. `php artisan key:generate`
4.  add `Schema::defaultStringLength(191)` at app/Providers/AppServiceProvider.php <br>
	(or)<br>
	In `config/database.php` file, need to set up <br>
	`'charset' => 'utf8mb4'` to `'charset' => 'utf8'` and <br>
	`'collation' => 'utf8mb4_unicode_ci'` to `'collation' => 'utf8_general_ci'`
5. `php artisan migrate`
6. `php artisan db:seed`
7. `php artisan serve`

The App will be running on `localhost:8000`.

This tutorial from [https://laravel-news.com/your-first-laravel-application](https://laravel-news.com/your-first-laravel-application)
