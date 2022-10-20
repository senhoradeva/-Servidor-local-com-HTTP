# Servidor local com HTTP

```Jsx
const http = require('http');

const port = 3000;

const rotas = {
    '/': 'Senhora Deva',
    '/sobre':'Informação sobre a plataforma' ,
    '/blog': 'Blog da Senhora Deva'
}

const server = http.createServer((req, res) => {
    res.writeHead(200, {'Content-Type': 'text/plain'});
    res.end(rotas[req.url]);
});

server.listen(port, () => {
    console.log(`Servidor escutando em http://localhost:${port}`);
});
```
