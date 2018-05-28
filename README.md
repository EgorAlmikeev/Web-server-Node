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
