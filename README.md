![logo](https://user-images.githubusercontent.com/68918326/193332767-8248edfa-cf76-4032-8eed-05bf3037838c.PNG)

<hr>
<h1 align="center">🎖️Aplicação Base - Laravel + Vue.js + Inertia.js🎖️</h1>
<hr>
<br>


<h2 align="center">Objetivo</h2>
<p align="center">
  Desenvolver um sistema base para ser utilizado e em todas as aplicações web futuras, tendo como padrão a utilização de tecnologias como Laravel, Vue.js e Inertia.js, tudo isso sem a utilização de kits de inicialização como breeze para iniciar o projeto</p>
<br>
<br>

<h2 align="center">🚧Configurando o Server-side🚧</h2>
<br>

  #### Criar o projeto laravel utilizando o composer
    📌 composer create-project --prefer-dist laravel/laravel nome-do-seu-projeto

  #### Instalar o adaptador do inertia no laravel
    📌 composer require inertiajs/inertia-laravel
  
  #### Criar um arquivo chamado app.blade.php, no diretório resources/views
    📌 Com o seguinte código:
![app-blade](https://user-images.githubusercontent.com/68918326/222423963-ff861496-654f-4bfc-a563-26d452d16889.PNG)


  #### Criar o middleware do inertia
    📌 php artisan inertia:middleware

  #### Acessar o arquivo App/Http/Kernel.php, e adicionar a linha abaixo ao arquivo:
    📌 \App\Http\Middleware\HandleInertiaRequests::class

<br>
<br>

<h2 align="center">🚧Configurando o Client-side🚧</h2>
<br>

  #### Instalar o laravel/ui
    📌 require laravel/ui

  #### Informar para o laravel que será usado o vue.js
    📌 php artisan ui vue
  
  #### Instalar as depedências do projeto
    📌 npm install

  #### Instalar as dependências do inertia para o client-side
    📌 npm install @inertiajs/inertia @inertiajs/inertia-vue3

  #### Modificar o arquivo resources/js/App.js, apagando todo o conteúdo e inserindo o código abaixo:
![app-js](https://user-images.githubusercontent.com/68918326/222426024-24e3c3fe-919a-4e41-9777-4b20137e5abb.PNG)

<br>
<br>

<h2 align="center">🚀Finalizando e testando instalação🚀</h2>
<br> 

  #### Criar uma pasta chamada "Pages"
    ✔️ Criar a pasta em resources/js, no mesmo nível que app.js

  #### criar um arquivo dentro da pasta "Pages" chamado Teste.vue 
    ✔️ Com a estrutura abaixo:
![teste](https://user-images.githubusercontent.com/68918326/222426782-e8f8f543-001b-4858-bfb6-8831d425f3b5.PNG)

  #### Criar um controller chamado TesteController
    ✔️ php artisan make:controller TesteController
    ✔️ Código do TesteController segue abaixo:
![TesteController](https://user-images.githubusercontent.com/68918326/222427246-1df966f7-f777-486d-9c83-9bf76171e2d8.PNG)

  #### Configurar a rota no arquivo routes/web.php
    ✔️ Route::get('/', [TesteController::class, 'index']);

  #### Inicie o servidor do laravel e a aplicação
    ✔️ php artisan serve
    ✔️ npm run watch


<br>
<br> 

![appJS](https://user-images.githubusercontent.com/68918326/184671337-013afa79-a43b-4c02-a808-5ae7befc4a1f.PNG)
<br>
<br>
