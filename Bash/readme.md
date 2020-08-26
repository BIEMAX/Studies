## Instalar certificados para seu projeto NODE JS

    https://timonweb.com/javascript/running-expressjs-server-over-https/
    https://stackoverflow.com/questions/8169999/how-can-i-create-a-self-signed-cert-for-localhost
    https://gist.github.com/cecilemuller/9492b848eb8fe46d462abeb26656c4f8
    https://gist.github.com/cecilemuller/a26737699a7e70a7093d4dc115915de8

    1. Rodar o seguinte comando no terminal:
    
    > openssl req -nodes -new -x509 -keyout server.key -out server.cert

    2. Ele irá criar um novo arquivo dentro da pasta raiz do node chamado *server.key*
    3. Em seguida irá solicitar o 'country name', digite 'BR' (sem apóstrofos)
    4. Em seguida irá solicitar o 'state or province name (full name)', digite 'Rio Grande do Sul'
    5. Em seguida irá solicitar o 'locality name', digite 'São Leopoldo'
    6. Em seguida irá solicitar o 'oganization name', digite 'doctorclin'
    7. Em seguida irá solicitar o 'organization unit name', digite 'administração'
    8. Em seguida irá solicitar o 'common name', digite 'localhost'
    9. No 'email address' não digite nada
    10. Ele irá criar um novo arquivo chamado *server.cert*


    Exemplo de informações no terminal:

    Country Name (2 letter code) [AU]:BR
    State or Province Name (full name) [Some-State]:Rio Grande do sul
    Locality Name (eg, city) []:São Leopoldo
    Organization Name (eg, company) [Internet Widgits Pty Ltd]:doctorclin
    Organizational Unit Name (eg, section) []:administração
    Common Name (e.g. server FQDN or YOUR name) []:localhost
    Email Address []:
    
    
```bash javascript
//define se a API irá aceitar somente chamadas em HTTPS
if (config.api.runAsHttps) {
  const https = require('https')
  const fs = require('fs')
  https.createServer(
    {
      key: fs.readFileSync('server.key'),
      cert: fs.readFileSync('server.cert')
    }, app)
    .listen(config.api.portServer || 3000, function () {
      console.log('Servidor da API HTTPS iniciado na porta ' + (config.api.portServer || 3000) + ' em ' + Date())
      console.log('--------------------------------------------------')
    })
}
else {
  // start server for API
  app.listen(config.api.portServer || 3000, function () {
    console.log('Servidor da API HTTP iniciado na porta ' + (config.api.portServer || 3000) + ' em ' + Date())
    console.log('--------------------------------------------------')
  })
}
```
