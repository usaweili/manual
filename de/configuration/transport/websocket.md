# WebSocket

[![English](../../resources/english.svg)](https://www.v2ray.com/en/configuration/transport/websocket.html) [![Chinese](../../resources/chinese.svg)](https://www.v2ray.com/chapter_02/transport/websocket.html) [![German](../../resources/german.svg)](https://www.v2ray.com/de/configuration/transport/websocket.html) [![Russian](../../resources/russian.svg)](https://www.v2ray.com/ru/configuration/transport/websocket.html)

Verwenden Sie den Standard-WebSocket, um Daten zu transportieren. Websocket-Verbindungen können von einem HTTP-Server wie Nginx weitergeleitet werden.

Aufbau:

```javascript
{"Pfad": "", "Kopfzeilen": {"Host": "v2ray.com"}}
```

Woher:

* `Pfad`: Pfad für WebSocket. Standard für root, wie `""`.
* `Header`: Benutzerdefinierter HTTP-Header. Ein Array, bei dem jeder Eintrag ein Schlüsselwertpaar in der Zeichenfolge, für den Header und den Wert im HTTP-Header ist. Der Standardwert ist leer.

## Beachten

* Seit V2Ray 3.4 erkennt Websocket den X-Forwarded-For-Header und verwendet ihn als Quelladresse des Datenverkehrs.