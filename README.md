

<h1 align="center"> WebSockets: implemente comunicações em tempo real com Socket.IO e MongoDB </h1>

<h2>1. Aplicar o fluxo de cadastro, login e armazenamento de JWT, na prática</h2>

Cadastramos senhas criptografadas;
Autenticamos os usuários e geramos o JWT no servidor, depois mandamos para o front-end;
Guardamos o JWT nos cookies, no front-end. Definimos e lemos um cookie, deletamos ao fazer logout, etc.

<h2>2. Controlar acessos</h2>

Utilizamos middlewares do Socket.IO para verificar a autenticidade do cliente. Registramos uma função middleware no servidor e ela, basicamente, concedia ou bloqueava ao acesso de um cliente tentando se conectar ao nosso servidor;
Para garantir que esse middleware fosse aplicado apenas nas páginas restritas do AluraDocs, nós criamos um namespace para registrar o middleware. Nomeamos nosso namespace como Usuarios, que apenas os usuários autenticados podem acessar.

<h2>3. Controlar informações localmente</h2>

Criamos uma lista local para controlar as conexões dos documentos, para saber qual usuário entrava em qual documento;
Utilizamos socket.data para armazenar as informações no socket. Usamos essa propriedade, especificamente, para conseguir saber se um usuário já havia entrado no documento ou não. Podemos usar essa propriedade para diversas finalidades, para implementar funcionalidades ainda mais avançadas no AluraDocs.

<h2 align="center"> Bibliotecas e dependências </h2>


```npm init -y``` - Cria um novo projeto em Node, o "-y" serve para responder "sim" as perguntas que o terminal faz

```npm install express@4``` - utilizamos para fazer um servidor Node básico


```npm install nodemon@2 -D``` - Serve para reiniciar o servidor automaticamente quando acontece uma modificação

```npm install socket.io@4``` - utilizamos a biblioteca Socket.IO, que permite trabalhar com o protocolo WebSockets de forma mais facilitada.

```npm install mongodb@4.11``` - adiciona o MongoDB como uma dependência

```npm install jsonwebtoken@8.5.1```  - Biblioteca para implementar o JWT

```npm install dotenv@16.0.3```  - Biblioteca para deixar a informação sensível mais segura