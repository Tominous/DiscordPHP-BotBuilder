## DiscordPHP-BotBuilder

Provides an easy way to make your own bot.

### Install

1. Get [Composer](https://getcomposer.org)
2. Run `composer init` and fill it out.
3. Run `composer require david-cole/discord-php-bot-builder`.
4. Include the `vendor/autoload.php` file.
5. Make a bot.

### Usage

```php
use Discord\Bot\Bot;

$config = [
	'prefix' => '!',
];

$bot = new Bot('token', $config);

/**
 * Will reply to `!hello` with 'Hello!'
 */
$bot->addComamnd('hello', function ($params, $message) {
	$message->reply('Hello!');
});

$bot->start();
```

A better example is provided in `example.php`.

### License

Covered by the MIT license:

```
The MIT License (MIT)

Copyright (c) 2015 David Cole <david@team-reflex.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```