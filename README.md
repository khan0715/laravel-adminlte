# Laravel Eloquent 5.8 + Adminlte2

## Getting Started

[AdminLTE](https://github.com/jeroennoten/Laravel-AdminLTE) - Code 


### Installing

```
composer require jeroennoten/laravel-adminlte
```

Laravel 5.8 uses Package Auto-Discovery, so doesn't require you to manually add the ServiceProvider

```
JeroenNoten\LaravelAdminLte\ServiceProvider::class,
```
Publish the public assets:
```
php artisan vendor:publish --provider="JeroenNoten\LaravelAdminLte\ServiceProvider" --tag=assets
```

##Updating

To update this package, first update the composer package:
```
composer update jeroennoten/laravel-adminlte
```
Then, publish the public assets with the --force flag to overwrite existing files

```
php artisan vendor:publish --provider="JeroenNoten\LaravelAdminLte\ServiceProvider" --tag=assets --force
```

## The make:adminlte artisan command


This package ships with a make:adminlte command that behaves exactly like make:auth (introduced in Laravel 5.2) but replaces the authentication views with AdminLTE style views.

```
php artisan make:adminlte
```


## Configuration

First, publish the configuration file:

```
php artisan vendor:publish --provider="JeroenNoten\LaravelAdminLte\ServiceProvider" --tag=config
```

## Menu

You can configure your menu as follows:

```
'menu' => [
    'MAIN NAVIGATION',
    [
        'text' => 'Blog',
        'url' => 'admin/blog',
    ],
    [
        'text' => 'Pages',
        'url' => 'admin/pages',
        'icon' => 'fas fa-fw fa-file'
    ],
    [
        'text' => 'Show my website',
        'url' => '/',
        'target' => '_blank'
    ],
    'ACCOUNT SETTINGS',
    [
        'text' => 'Profile',
        'route' => 'admin.profile',
        'icon' => 'fas fa-fw fa-user'
    ],
    [
        'text' => 'Change Password',
        'route' => 'admin.password',
        'icon' => 'fas fa-fw fa-lock'
    ],
],
```

## Translations

At the moment, English, German, French, Dutch, Portuguese and Spanish translations are available out of the box. Just specifiy the language in config/app.php. If you need to modify the texts or add other languages, you can publish the language files:

```
php artisan vendor:publish --provider="JeroenNoten\LaravelAdminLte\ServiceProvider" --tag=translations

```

## Customize views

If you need full control over the provided views, you can publish them:

```
php artisan vendor:publish --provider="JeroenNoten\LaravelAdminLte\ServiceProvider" --tag=views

```
