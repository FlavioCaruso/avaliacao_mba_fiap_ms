## Atividade FIAP - Desenvolvimento de microsserviços e API

<h2 align="center">Configurações</h2>

### Dependências :warning:

<b>1</b> - Acesse a pasta Financeiro e rode o comando:

```shell
npm install
```

<b>2</b> - Acesse a pasta Usuario e rode o comando:

```shell
npm install
```

---

### Configuração do MongoDB :shield:

<b>1</b> - Acesse o arquivo Financeiro/src/config/cfg.js e altere o db_path:<br>

```js
"mongodb+srv://*****:*****@*****.*****.mongodb.net/*****?retryWrites=true&w=majority";
```

para sua conexão de banco de dados.<br><br>
<b>2</b> - Acesse o arquivo Usuario/src/config/cfg.js e altere o db_path:<br>

```js
"mongodb+srv://*****:*****@*****.*****.mongodb.net/*****?retryWrites=true&w=majority";
```

para sua conexão de banco de dados.<br>

---

### Inicializando :heavy_check_mark:

<b>1</b> - Acesse a pasta Financeiro e rode o comando:<br>

```shell
npm run dev
```

Será inicializado um servidor em: [http://localhost:3001](http://localhost:3001).

<b>2</b> - Acesse a pasta Usuario e rode o comando:<br>

```shell
npm run dev
```

Será inicializado um servidor em: [http://localhost:3000](http://localhost:3000).

<h2 align="center">Rotas</h2>

### Usuários :standing_person:

<b>LISTAR</b> - [GET] [http://localhost:3000/usuarios](http://localhost:3000/usuarios) --header token<br>
<b>CADASTRO</b> - [POST] [http://localhost:3000/usuarios/cadastro](http://localhost:3000/usuarios/cadastro)<br>
<b>AUTENTICAÇÃO</b> - [POST] [http://localhost:3000/usuarios/login](http://localhost:3000/usuarios/login)<br>
<b>TROCA SENHA</b> - [POST] [http://localhost:3000/usuarios/altera-senha](http://localhost:3000/usuarios/altera-senha) --header token<br>

### Financeiro :dollar:

<b>LISTAR</b> - [GET] [http://localhost:3001/financeiro](http://localhost:3001/financeiro) --header token<br>
<b>CADASTRO</b> - [POST] [http://localhost:3001/financeiro/cadastro](http://localhost:3001/financeiro/cadastro) --header token<br>
<b>UPDATE</b> - [PUT] [http://localhost:3001/financeiro/:id](http://localhost:3001/financeiro/:id) --header token<br>
