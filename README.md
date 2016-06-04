#  OneSignal Push Notifications for Laravel 5

## Introduction

This project is a wrapper for the OneSignal v1 API.  It supports all operations currently supported by the API.

## Installation (Laravel and Lumen)

Require the package with composer.

```sh
composer require Jmrieger/onesignal-laravel
composer update
```

## Laravel Users:
Update `config/app.php` by adding the following entries.
```php
'providers' => [
	// ...
	Jmrieger\OneSignal\OneSignalServiceProvider::class
];

'aliases' => [
   	// ...
   	'OneSignal' => Jmrieger\OneSignal\OneSignalFacade::class
   ];
```

## Lumen Users:
update `bootstrap/app.php`, adding the following entry
```php
$app->register( \Jmrieger\OneSignal\OneSignalServiceProvider::class );
class_alias( 'Jmrieger\OneSignal\OneSignalFacade', 'OneSignal' );
```


## Configuration
There are 3 settings that need to be updated: your default OneSignal app ID, the REST API key, and the User Auth Key.  All of these items can be found in your Control Panel on the OneSignal site.

Place the 3 keys into your .env file, as such:
```
ONESIGNAL_APP_ID=
ONESIGNAL_REST_API_KEY=
ONESIGNAL_USER_AUTH_KEY=
```

## Usage



## References
The official OneSignal API documentation is listed here:
https://documentation.onesignal.com/docs/server-api-overview


## Acknowledgements
This project was inspired by, and evolved from, https://github.com/berkayk/laravel-onesignal