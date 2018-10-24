# monolog-rocketchat-handler

[![Build Status](https://travis-ci.org/martinusso/monolog-rocketchat-handler.svg?branch=master)](https://travis-ci.org/martinusso/monolog-rocketchat-handler)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/?branch=master)
[![Build Status](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/badges/build.png?b=master)](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/build-status/master)
[![Code Intelligence Status](https://scrutinizer-ci.com/g/martinusso/monolog-rocketchat-handler/badges/code-intelligence.svg?b=master)](https://scrutinizer-ci.com/code-intelligence)

[![License](https://poser.pugx.org/martinusso/monolog-rocketchat-handler/license)](https://packagist.org/packages/martinusso/monolog-rocketchat-handler)
[![Latest Stable Version](https://poser.pugx.org/martinusso/monolog-rocketchat-handler/v/stable)](https://packagist.org/packages/martinusso/monolog-rocketchat-handler)
[![Latest Unstable Version](https://poser.pugx.org/martinusso/monolog-rocketchat-handler/v/unstable)](https://packagist.org/packages/martinusso/monolog-rocketchat-handler)
[![composer.lock](https://poser.pugx.org/martinusso/monolog-rocketchat-handler/composerlock)](https://packagist.org/packages/martinusso/monolog-rocketchat-handler)
[![Total Downloads](https://poser.pugx.org/martinusso/monolog-rocketchat-handler/downloads)](https://packagist.org/packages/martinusso/monolog-rocketchat-handler)


## Dependecies

- Monolog


## Installation

```
composer require martinusso/monolog-rocketchat-handler
```


## Usage

Push this handler to your Monolog instance:

```php
$webhook = 'https://rocket.chat.local/hooks/bd97pizfGu3S5q5oT/SmCgGWSc4vEuRyBu5eocnBDDKvZvoqL6whRKpvsBK2TjvNk2';

$rocketChatHandler = new RocketChatHandler\RocketChatHandler([$webhook], Monolog\Logger::DEBUG);

$monolog = new Monolog\Logger('Rocket.Chat');
$monolog->pushHandler($rocketChatHandler);
```

Supports multiple webhook URLs:

```php
$rocketChatHandler = new RocketChatHandler\RocketChatHandler(
    [
        'https://rocket.chat.local/hooks/bd97pizfGu3S5q5oT/SmCgGWSc4vEuRyBu5eocnBDDKvZvoqL6whRKpvsBK2TjvNk2',
        'https://rocket.chat.server/hooks/bd97pizfGu3S5q5oT/SmCgGWSc4vEuRyBu5eocnBDDKvZvoqL6whRKpvsBK2TjvNk2',
        // ...
    ],
    Monolog\Logger::DEBUG
);

// ...
```


## License

This software is open source, licensed under the The MIT License (MIT). See [LICENSE](https://github.com/martinusso/monolog-rocketchat-handler/blob/master/LICENSE) for details.
