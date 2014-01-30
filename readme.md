# multi-app-laravel

[multi-app-laravel](http://github.com/rbewley4/multi-app-laravel) is a template [Laravel](http://laravel.com/) project
that supports multiple applications.


## Changes from stock Laravel

1. Each application is stored in `./applications/<application-name>` instead of `./app`.
2. Applications are completely independent of one another (separate `public`, `config`, etc. directories), but they share Laravel bootstrap files, and vendor libraries. 
3. A library was added that is accessible to all applications. They automatically include `./lib` in `global.php`.
4. Unit tests do not work yet


## Installation

### 1. Download the Code

This is as simple as using git to clone the repo:

```bash
git clone git@github.com:rbewley4/multi-app-laravel.git
```

### 2. Download Dependencies

All dependencies are listed in the `composer.json` file, and can be downloaded via [composer](https://getcomposer.org/):

```bash
cd multi-app-laravel
composer install
```

### 3. Configure Your Application

**mulit-app-laravel** comes with a sample Laravel application installed in `./applications/myapp`. You can rename
it without harming anything:

```bash
cd applications
mv myapp mynewapp
```

Once you have renamed it to your liking, you can configure your application like any other Laravel application:
* add routes to `myapp/routes.php`
* edit config files in `myapp/config/`

### 4. Create Additional Applications

If you want to create an additional application, simply copy the entire `myapp` directory and rename it as desired. Your new application has its own public directory, and its own configuration files, but shares the common files stored in the lib directory.

### 5. Configure Webserver

The only difference between **multi-app-laravel** and **Laravel** in terms of configuring the webserver, is that 
**multi-app-laravel** has multiple applications, each of which need to have their own virtual host. Just point the document root for each virtual host at the `public` directory of one of the applications. 


## License

This project is derived from version 4.0.7 of Laravel, and is licensed under the same terms:
[MIT license](http://opensource.org/licenses/MIT).
