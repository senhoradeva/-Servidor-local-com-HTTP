# Servidor local com HTTP
<ul>
 <li>Crie uma pasta onde para seu projeto</li>
  <li>Digite o comando npm init -y</li>
  <li>Crie o arquivo server.js copie e cole o código abaixo</li>
  <li>Abra o terminal e digite node server.js - vai aparecer http://localhost:3000, copie o caminho e cole no navegador.</li>
</ul>



Vamos usar o nodemon para não que para o servidor e subir de novo a cada nova atualização, para isso npm install nodemon -D

No package.json digite o seguinte script: 
```Jsx
 "scripts": {
    "start": "nodemon server.js"
  },
```

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
