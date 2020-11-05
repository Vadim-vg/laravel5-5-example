## Laravel 8 example rus ##

**Laravel 8 example** Это учебное приложение.

### Установка ###

* команда `git clone https://github.com/bestmomo/laravel8-example.git projectname` клонирует репозиторий с помощью командной строки
* команда `cd projectname` перейдёт в папку проекта
* команда `composer install` установит зависимости с помощью программы "composer" (произойдёт установка всех зависимостей проекта указанных в файле `composer.json` с версиями указанными в `composer.lock`)
* команда `composer update`
* скопировать *.env.example* в *.env*
* команда `php artisan key:generate` cгенерирует ключ безопасности в файле *.env*
* Если вы используете MySQL в файле *.env* укажите параметры подключения:
* Тип БД DB_CONNECTION=mysql
   * название БД DB_DATABASE
   * имя пользователя DB_USERNAME
   * пароль пользователя DB_PASSWORD
* Если вы используете sqlite :
   * команда `touch database/database.sqlite` создаст файл
* команда `php artisan vendor:publish --provider="Bestmomo\LaravelEmailConfirmation\ServiceProvider" --tag="confirmation:migrations"` опубликует миграцию подтверждения электронной почты
* команда `php artisan migrate --seed` создаст и заполнит таблицы
* редактируйте *.env* для конфигурирования электронной почты

### Include ###

* [Styleshout](https://www.styleshout.com/) for front template
* [CKEditor](http://ckeditor.com) the great editor
* [Elfinder](https://github.com/Studio-42/elFinder) the nice file manager
* [Sweet Alert](http://t4t5.github.io/sweetalert/) for the cool alerts
* [AdminLTE](https://adminlte.io/themes/AdminLTE/index2.html) the great admin template
* [Gravatar](https://github.com/creativeorange/gravatar) the Gravatar package
* [Intervention Image](http://image.intervention.io/) for image manipulation
* [Email confirmation](https://github.com/bestmomo/laravel-email-confirmation) the package for email confirmation
* [Artisan language](https://github.com/bestmomo/laravel-artisan-language) the package for language strings management
* [Laravel debugbar](https://github.com/barryvdh/laravel-debugbar)
* [Etrepat baum](https://github.com/etrepat/baum) for comments management

### Features ###

* Home page
* Custom error pages 403, 404 and 503
* Authentication (registration, login, logout, password reset, mail confirmation, throttle)
* Users roles : administrator (all access), redactor (create and edit post, upload and use medias in personnal directory), and user (create comment in blog)
* Blog with nested comments
* Search in posts
* Tags on posts
* Contact us page
* Admin dashboard with users, posts, articles, medias, settings, notifications and comments
* Multi users medias gestion
* Localization (English, French and Chinese)
* Application tests
* Thumbs creation for images
* Notifications to send emails and notify redactors for new comments

### Tricks ###

To use application the database is seeding with users :

* Administrator : email = admin@la.fr, password = admin
* Redactor : email = redac@la.fr, password = redac
* User : email = walker@la.fr, password = walker
* User : email = slacker@la.fr, password = slacker

### Tests ###

When you want to launch the tests refresh and populate the database :

`php artisan migrate:fresh --seed`

You must have default settings and **en** language. You must also add provider in **config/app.php**.

You can then use Dusk.

### License ###

This example for Laravel is open-sourced software licensed under the MIT license
