# PHP Library to Calculate Fajr and Isha Timings per MoonSighting.com

## Requirements
* PHP 7.3+

## Install
```php
composer install islamic-network/prayer-times-moonsighting
```

## Usage
To calculate Fajr minutes before sunrise:

```php
use IslamicNetwork\MoonSighting\Fajr;
use DateTime;

$date = new DateTime('24-12-2020');
$pt = new Fajr($date, 25.2119894);
$pt->getMinutesBeforeSunrise(); // 88 minutes
```

To calculate Isha minutes after sunset:

```php
use IslamicNetwork\MoonSighting\Fajr;
use DateTime;

$date = new DateTime('24-12-2020');
$pt = new Isha($date, 25.2119894);
$pt->getMinutesAfterSunset(); // 86 minutes
```

## Tests
To run unit tests, from the root of this repository execute:

```php
vendor/bin/phpunit tests/Unit/
```