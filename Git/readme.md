## Links auxiliares

https://docs.github.com/en/github/managing-files-in-a-repository/getting-permanent-links-to-files

## Extensões recomendáveis

  Antes de iniciar os estudos no visual code e o git, você deve instalr as seguintes extensões no visual studio code:
  
  > GitHub Pull Requests and Issues (https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
  
  > Dotenv (https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv)
  
  > GitLens — Git supercharged (https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
  
  > Live share *opcional* (https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)
  
  > TODO List *opcional* (https://marketplace.visualstudio.com/items?itemName=TzachOvadia.todo-list)
  
## Configurações recomendáveis de padrão de código

  **ESLint**
  
  > O ESLint é uma ferramenta para identificar e relatar padrões encontrados no código ECMAScript / JavaScript, com o objetivo de tornar o código mais consistente e evitar erros de formatação. De muitas maneiras, é semelhante ao JSLint e JSHint (https://eslint.org/docs/user-guide/getting-started#:~:text=ESLint%20is%20a%20tool%20for,uses%20Espree%20for%20JavaScript%20parsing.)
  
  ```javascript
  //Exemplo de arquivo ".eslintrc.js"
  module.exports = {
    env: {
      es6: true,
      node: true,
    },
    extends: 'eslint:recommended',
    parserOptions: {
      ecmaVersion: 2017,
    },
    globals: {
      __: false,
      describe: false,
      before: false,
      it: false,
    },
    rules: {
      indent: ['error', 2],
      'linebreak-style': ['error', 'unix', 'windows'],// unix para linux e windows para windows
      quotes: ['error', 'single'],
      semi: ['error', 'never'],
    },
  };
  ```
  
## Configuração do git

  Após criar o seu código local, está na hora de você integrar ao github para controle de commits, pull e issue requests. Para isso, deve ser seguido os passos abaixo:
  
  1. Fazer o login no github (após a instalação da extensão) ao lado esquerdo do visual code, terá um ícone acima do *símbolo da engrenagem* que dá acesso às configurações.
  
  2. Agora feito o login, você deverá configurar o seu **visual studio code** para identificar seus commits. Para isso, deverá ser criado um arquivo chamado *.gitconfig* (localização do arquivo abaixo).
  
  > Em sistemas operacionais Windows: *C:\Users\<SeuUsuarioWindowsAqui>\.gitconfig
  
  > Em sistemas operacionais linux: *Unkown*
  
  3. Para configurar, basta executar os comandos abaixos (um por vez), respeitando sua cronologia:
  
  > **Atenção**: Extremamente recomendável seguir os passos para não ter problemas e/ou complicações.
  
  4. O jeito mais fácil (e menos trabalhoso) de efetuar seus commits é criar um repositório (pasta) dentro do Github (pode ser uma pasta vazia apenas com o arquivo de licença MIT) e efetuar um git clone.
  
  5. Após obter o git clone do seu repositório, abra um diretório em um local de sua escolha no seu sistema operacional e navegue com o terminal (cmd, powershell, terminal do linux) até o mesmo e digite o seguinte comando:
  ```bash
  git clone <url>
  ```
  
  6. Isso fará com que o terminal faça um download do seu diretório e já efetue as configurações básicas para enviar commits (enviar seu código para nuuvem). Você pode optar por configurar por conta e risco, o que é extremamente difícil e cansativo. Em seguida, você precisará configurar o seu usuário e e-mail, para que quando efetue um commit, fique salvo quem foi o responsável por fazê-lo.
  
  > **Atenção:** Os comandos abaixo não funcionaram na minha máquina (não ficou definido o usuário por algum motivo desconhecido), por isso, tive que seguir com o passo 4.
  
  > Comandos que o Git apresenta
  ```bash
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
  ```
  
  > Comandos de exemplo
  ```bash
  git config --global user.email "dionei@google.com"
  git config --global user.name "Dionei dos santos"
  ```
  
  > **Aviso:** Os exemplos que contenham menor/maior e aspas devem ser removidos ao configurar no seu ambiente, eles estão presentes apenas 
  
  > Configurar o nome de usuário responsável pelo commits
  ```bash
  git config user.name <"SeuNomeAqui">
  ``` 
  
  > Configura o e-mail do usuário responsável pelos commits
  ```bash
  git config user.email <"SeuEmailAqui@someplace.com">
  ```
  
  ## Comandos úteis do GIT
  
  > Incrementar a versão do package json (version) automaticamente
  ```
  npm version patch --force
  ```
  
  ## Sequência de comandos do GIT
  
  1. Após configurar seu git no seu projeto local, você poderá iniciar o seu desenvolvimento. Após adicionar/editar/excluir algo no seu código, os comandos a serem seguidos são:
  ```bash
  git add *
  git add .
  git add -A
  ```
  > **Outros códigos git com a mesma funcionalidade do código acima:**
  ```bash
  git add -A
  git commit -a -m "Sua mensagem de commit aqui"
  ```
  
  2. Após efetuar o stage dos seus arquivos, efetuar o commit (exceto se ele não foi executado com o segundo comando acima, caso o commit já tenha sido executado, prosseguir para o passo de número oito (8)):
  ```bash
  git commit -m "some init msg"
  ```
  
  3. O commit fica salvo na sua máquina, você deverá enviá-lo para nuvem (github, bitbucket, dentre outros serviços) utilizando o seguinte comando:
  ```bash
  git push "respository name" "branch"
  ```
  > **Aviso:** O nome acima deve ser o mesmo dado no passo de número 6. Só será necessário informar o nome do repositório e branch caso tu não tenha clonado o projeto diretamente do git hub.
  
  > **Aviso 2:** A branch é o nome da sua branch ou feature que estiver trabalhando (master, develop, feature/I107, etc...)
