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
  
  Adicionar o usuário ao *grupo sudo* no CentOs:
  > usermod -aG sudo UserNameHere
  
  > **e.g.:** usermod -aG sudo proxy
    
  Adicionar o usuário ao *grupo sudo* no Linux:
  > usermod -G root UserNameHere
  
  > **e.g.:** usermod -G root dcapihml
  
  Obter a lista de usuários do linux:
  > cat /etc/passwd
  
  > **Aviso:** Caso algum usuário listado esteja dentro da pasta *nologin*, significa que o mesmo não tem acesso para efetuar logins dentro do linux. Para habilitá-lo, inserir o comando abaixo:
  
  > sudo chsh -s /bin/bash UserNameHere
  
  Trocar a senha de algum usuário:
  > sudo passwd UserNameHere
  
  Dar permissões nas pastas:
  > sudo chmod a+rwx /path/to/file
  
  **e.g.:**
  > sudo chmod a+rwx /opt
  
  
  Ferramenta para download de arquivos:
  > sudo apt-get install wget
  
  *Como utilizar:*
  > wget UrlHere
  >
  > **e.g.:** wget https://download.oracle.com/otn_software/linux/instantclient/19600/instantclient-basic-linux.x64-19.6.0.0.0dbru.zip
  
  
  Decompactador de arquivos linux:
  > sudo apt-get install unzip
  
  *Como utilizar:*
  > wget UrlHere
  >
  > **e.g.:** unzip file.zip -d /opt/DestinationFolderHere
  
## Instalação de aplicativos
  
  Instalar o editor de texto nano para *linux ubuntu e debian*:
  > sudo apt install nano
  
  Instalar o editor de texto vim para *linux ubuntu e debian*:
  > sudo apt install vim
  
  Instalar o reddis:
  > sudo apt install redis-server
  
  
## Documentações
  
  [Clique aqui](https://linuxize.com/post/how-to-use-nano-text-editor) para visualizar uma documentação básica (e bem útil) para uso do nano em terminais.
  [Clique aqui](https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-18-04-pt) para visualizar uma documentação de instalação do servidor redis.
  

## Configurações

  Para alteração do hostname do seu linux server/client, [clique aqui](https://www.cyberciti.biz/faq/ubuntu-change-hostname-command/).
  
  Para habilitar o firewall na inicialização do status:
  > sudo ufw enable
  
  Para verificar aplicativos com exceções no firewall:
  > sudo ufw status
  
  Habilitar o login como root (por padrão, esse login é desativado em distros linux):
  
  > [Clique aqui](https://linuxconfig.org/allow-ssh-root-login-on-ubuntu-20-04-focal-fossa-linux) para habilitar o login com o usuário *root* no linux ubuntu
