Intercom
===============

Wrapper on the Intercom class provided by Intercom  - with support for Laravel 9.x

Installation
------------

Installation using composer:

```
composer require darkin1/intercom
```


And add the service provider in `config/app.php`:

```php
Darkin1\Intercom\IntercomServiceProvider::class,
```

And add the facade alias in `config/app.php`:

```php
'Intercom'  => Darkin1\Intercom\Facades\Intercom::class,
```

Configuration
-------------

Change your default settings in `app/config/intercom.php`:

```php
<?php
return [
    'access_token' => env('INTERCOM_ACCESS_TOKEN', '****'),
    'api_version' => env('INTERCOM_API_VERSION', '1.1'),
];
```

Review the official docs to see the list of [available intercom api versions](https://developers.intercom.com/intercom-api-reference/reference)

Example
-------------

```php

use Intercom;

$users = Intercom::users()->getUsers([]);

$leads = Intercom::leads()->getLeads([]);

```


Documentation
-------------

[Intercom API](https://github.com/intercom/intercom-php)

