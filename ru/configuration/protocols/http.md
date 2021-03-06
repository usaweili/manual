# HTTP

[![Английский](../../resources/english.svg)](https://www.v2ray.com/en/configuration/protocols/http.html) [![Китайский](../../resources/chinese.svg)](https://www.v2ray.com/chapter_02/protocols/http.html) [![Немецкий](../../resources/german.svg)](https://www.v2ray.com/de/configuration/protocols/http.html) [![Русский](../../resources/russian.svg)](https://www.v2ray.com/ru/configuration/protocols/http.html)

HTTP - это протокол для входящих соединений. Он совместим с HTTP 1.1.

* Название: http
* Тип: входящий
* Конфигурация:

```javascript
{
  "accounts": [
    {
      "user": "my-username",
      "pass": "my-password"
    }
  ],
  "allowTransparent": false,
  "userLevel": 0
}
```

Где:

* `accounts`: Массив, в котором каждая запись является учетной записью. Имя пользователя указывается через `user`, а пароль через `pass`. Значения по умолчанию пустые. 
  * Если значение `accounts` не пустое, HTTP использует базовую аутентификацию для подтверждения пользователя.
* ` allowTransparent `: Если установлено значение ` true `, все полученные HTTP-запросы, будут проксированы, включая запрос без прокси.
* ` userLevel `: Пользовательский уровень. Все подключения проходят через этот уровень.

## Советы

Используйте следующие настройки в Linux для использования прокси-сервера HTTP в текущем сеансе.

* `export http_proxy=http://127.0.0.1:8080/` (Адрес должен быть изменён на требуемый)
* `export https_proxy=$http_proxy`