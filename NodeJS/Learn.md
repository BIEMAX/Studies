## Links auxiliares

https://scotch.io/tutorials/easy-node-authentication-setup-and-local

https://www.guru99.com/node-js-modules-create-publish.html

https://code.visualstudio.com/docs/nodejs/nodejs-tutorial

https://nodejs.org/en/docs/guides/getting-started-guide/

https://developer.mozilla.org/pt-BR/docs/Learn/Server-side/Express_Nodejs/ambiente_de_desenvolvimento

## Criando um novo projeto

Para criar um novo projeto, basta criar uma nova pasta em um local de sua escolha em seu computador.
  
  1. C:\Users\Dionei\Desktop\NewNodeApp
  
  2. Rodar o comando abaixo para criar o arquivo de dependências *package.json*:
  ```bash
  npm init
  ```
  
  3. Após isso, instalar o npm express (biblioteca avançada para manipulação de NodeJS, com fácil implementação) executando o seguinte comando:
  ```bash
  npm install express
  ```
  
  > **Aviso:** Para maiores informações sobre o npm express, acessar o link https://www.npmjs.com/package/express
  
  4. Instalar o *nodemon* nas dependências do dev, para facilitar o desenvolvimento e iniciar o servidor com o comando:
  
  > Comando para instalar o *nodemon* apenas para ambiente de desenvolvimento:
  
  ```
  npm install --save-dev nodemon
  ```
  
  ```bash
  npm run dev
  ```
  
  5. Após instalar o *nodemon*, basta adicionar no *package.json*, as inicializações (exemplo a seguir):
  ```json
  {
    "name": "smart-assistant-api",
    "version": "1.0.0",
    "description": "API for query database information",
    "main": "index.js",
    "scripts": {
    "dev": "nodemon index.js",
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
    "author": "",
    "license": "ISC",
    "dependencies": {
      "express": "^4.17.1"
    },
    "devDependencies": {
      "eslint": "^7.5.0",
      "nodemon": "^2.0.4"
    }
  }
  ```
  
  6. Instalar a dependência do Microsoft SQL Server.
  ```bash
  npm install -S mssql
  ```
