## Comandos úteis LINUX
  
  Navegar dentro de pastas (pode-se informar o caminho inteiro desejado
  > cd /FolderName/SubFolderName/etc..
  
  Inspecionar arquivos e pastas dentro de um diretório
  > ls
  
  Obter e ler um arquivo:
  > cat /FolderName/FileName.extension
  
  > **e.g.:** cat /etc/hosts
  
  Obter a versão do linux:
  > cat /etc/os-release
  
  Verificar o histórico de comandos (todos os comandos):
  > cat .bash_history
  
  Pesquisar por um comando dentro do histórico de comandos:
  > cat .bash_history | grep cert
  
  Verificar status do serviço:
  > service ServiceNameHere status

  Reiniciar um serviço:
  > service ServiceNameHere restart

  Fazer/trocar o login como/para root ou um usuário de sua escolha:
  > su root
  
  > **Aviso:** Irá solictar a senha do root ou do usuário informado
  
  Instalar pacotes ou até mesmo aplicações:
  > apt install PackageName
  
  > **e.g.:** apt install rpm
 
  Reiniciar o linux:
  > sudo reboot
  
  Adicionar um novo usuário:
  > adduser UserNameHere
  
  > **e.g.:** adduser proxy
  
  Adicionar o usuário ao *grupo sudo*:
  > usermod -aG sudo UserNameHere
  
  > **e.g.:** usermod -aG sudo proxy
  
  Obter a lista de usuários do linux:
  > cat /etc/passwd
  
  > **Aviso:** Caso algum usuário listado esteja dentro da pasta *nologin*, significa que o mesmo não tem acesso para efetuar logins dentro do linux. Para habilitá-lo, inserir o comando abaixo:
  
  > sudo chsh -s /bin/bash UserNameHere
  
  Trocar a senha de algum usuário:
  > sudo passwd UserNameHere
  
## Instalação de aplicativos
  
  Instalar o editor de texto nano para *linux ubuntu e debian*:
  > sudo apt install nano
  
  Instalar o editor de texto vim para *linux ubuntu e debian*:
  > sudo apt install vim
  
  
## Documentações
  
  [Clique aqui](https://linuxize.com/post/how-to-use-nano-text-editor) para visualizar uma documentação básica (e bem útil) para uso do nano em terminais.
  

## Configurações

  Para alteração do hostname do seu linux server/client, [clique aqui](https://www.cyberciti.biz/faq/ubuntu-change-hostname-command/).
  
