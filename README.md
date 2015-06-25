# TelegramBot API

This library wraps the [TelegramBot API](https://core.telegram.org/bots) and can be used to interact with bots generated by using [BotFather](https://core.telegram.org/bots#botfather)

## Installation

``` nodejs
npm install telegrambot
```

## Available Methods

All methods available on the API can be access using this library. The list of methods and expected results can be found in the [Bot API document](https://core.telegram.org/bots/api).

## Usage

``` nodejs
var TelegramBot = require('telegram-bot');

var api = new TelegramBot('<YOUR TOKEN HERE>');

api.invoke('getMe', {}, function (err, me) {
    if (err) throw err;
    console.log(me);
});

api.invoke('sendMessage', { chat_id: 1, text: 'my message' }, function (err, message) {
    if (err) throw err;
    console.log(message);
});