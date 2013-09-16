## multi-app-laravel

[multi-app-laravel](http://github.com/rbewley4/multi-app-laravel) is a template [Laravel](http://laravel.com/) project
that supports multiple applications.

## Changes from stock Laravel

1. Each application is stored in `./applications/<application-name>` instead of `./app`.
2. Each application has its own `public` directory, and its own `artisan` script.
3. You can put common code in the `./lib` directory. All applications automatically include this directory in
`global.php`.

## Create a new Application

To create a new application, simply copy the entire `myapp` directory and rename it as desired. Your new application
has its own public directory, and its own configuration files, but shares the common files stored in the lib directory.

## TODO

1. Update unit tests to support multiple applications.

## License

This project is derived from version 4.0.7 of Laravel, and is licensed under the same terms:
[MIT license](http://opensource.org/licenses/MIT).
