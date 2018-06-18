# Web-server-Node

[c9/Almikeev/13-03-2017 веб-сервер Node](https://ide.c9.io/gossoudarev/js-study1)

### index.js
```javascript
const http = require('http');
const moment = require('moment');
const server = http.createServer();

server.listen(4321);
server.on('request', (req, res) => {
	res.setHeader('Content-Type', 'application/json; charset=utf-8');
	res.end(JSON.stringify( { date : moment().format('DD.MM.YYYY HH:mm:ss') } ));
});
```

### log.txt
```bash
HTTP/1.1 200 OK
X-Powered-By: Express
Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: GET,POST,DELETE
Access-Control-Allow-Headers: Content-Type, Access-Control-Allow-Headers
Content-Type: application/json; charset=utf-8
X-By: Ilya Goss (c)2017
X-Test: POST34c29de28c1a5114a33fd0d437e84b41
Content-Length: 131
ETag: W/"83-vrm3tH4iCSuiE50zLaT6pg"
set-cookie: connect.sid=s%3AZ5jKQyCdZsJfF1gyUWkqzaiYfgu7pWNJ.M3NoSkJnPnL7MGbH7djWyCOE7fyS9bdi9tNGrLkMgUY; Path=/; Expires=Tue, 13 Mar 2018 14:22:44 GMT; HttpOnly
Date: Tue, 13 Mar 2018 11:36:04 GMT
Connection: close

{"name":"%D0%95%D0%B3%D0%BE%D1%","familyname":"Альмикеев\r\n\r\n\r\n\r","_METHOD":"POST","_NAME":"%D0%95%D0%B3%D0%BE%D1%"}
```
