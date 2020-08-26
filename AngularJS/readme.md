## Criando um novo projeto

1. Para criar um novo projeto, navegue até um diretório/paste de sua escolha.

> e.g.: C:\Users\Dionei\Desktop\NewNodeApp

2. Segure a tecla *shift* e pressione o botão direito do mouse sobre o diretório, em seguida, selecione a opção *Abrir janela do powershell aqui*.

4. Execute o comando abaixo para criar um novo projeto em angular.js

> ng new folder-name-here

5. Após isso, basta aprir o seu diretório dentro do *visual studio code* e executar o comando:

> ng serve

6. Acesse seu navegador e digite o seguinte endereço na URL:

> localhost:4200
>
> **Aviso:** Essa é a porta padrão de qualquer projeto *front end*

7. Caso desejar iniciar o projeto em uma porta distinta e/ou iniciar um outro projeto em paralelo, basta digitar o seguinte comando:

> ng serve --port 4218
> 
> **Aviso:** Certifique-se se a porta que você está tentando utilizar já não possuí algo em execução, pois caso estiver, o terminal do visual studio code apresentará um erro.


## Instalação de dependências

Caso você desejar, você poderá adicionar o *angular materials*, um framework contendo componentes personalizados com base no angular. Para adicioná-lo, basta executar o seguinte comando:
> ng add @angular/material

> **Aviso:** Você até consegue criar um projeto em Angular.JS e adicionar o Angular Material, mas é complexo demais, é mais simples criar um projeto novo utilizando o Material. Para isso, execute os comandos abaixos:

```bash
ng new angular-material-app
```

> **Aviso:** Maiores informações, [clique aqui.](https://tudip.com/blog-post/how-to-install-angular-material/)

Caso você preferir, poderá também instalar o *angular pwa* que significa *progressive web applications*, ou seja, combinam o que tem de melhor em aplicações Web e o melhor dos aplicativos.
> ng add @angular/pwa

Caso você deseja instalar em produção o seu projeto, deverá executar o seguinte comando:
> ng build --prod

## Fast tips

Para criar um novo componente dentro do seu projeto (sem ter de criar os componentes manualmente), digite o comando abaixo no seu terminal do *visual studio code*:

> ng generate component component-name-here

Ou utilizando a forma abreviada:

> ng g c component-name-here

> **Aviso:** Evite utilizar nomes de componentes com espaços, não é seguro (acredito que o Angular se quer permite isso).

Sempre que foi adicionado um novo componente, você precisará adicioná-lo manualmente nas rotas, dentro do arquivo *src/app-routing.module.ts* conforme exemplo abaixo:
```javascript
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { HomeComponent } from './home/home.component'; //Importação dos componentes criados anteriormente
import { LoginComponent } from './login/login.component'; //Importação dos componentes criados anteriormente

//Router to access through angular
const routes: Routes = [
  {
    path: '',//Caminho que a rota (url) será chamada para acessar o componente específico (se deixar em branco significará que é a página inicial)
    component: LoginComponent
  }
  ,{
     path: 'home', //Rota personalizada, não é necessário adicionar a barra ou contra barra, próprio framework faz isso
     component: HomeComponent
  }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```
Para inicializar o projeto em https ao invés de http:
> ng serve --ssl true
