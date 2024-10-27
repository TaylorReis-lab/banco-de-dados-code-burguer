# Banco de Dados - Web Code Borguer

Este projeto de banco de dados utiliza um sistema de gerenciamento de dados com suporte a PostgreSQL, MongoDB e armazenamento de imagens. Ele conta com migrações que definem a estrutura de tabelas para usuários, produtos, categorias, entre outros. Além disso, o sistema realiza verificações para evitar duplicidade de usuários com o mesmo email e gerencia o upload de imagens para produtos.

## Estrutura do Projeto

A estrutura do projeto é organizada da seguinte forma:

WEB-ORDER-CODE/ </br>
├── src/</br>
│   ├── app/</br>
│   │   ├── controllers/</br>
│   │   ├── middlewares/</br>
│   │   ├── models/</br>
│   │   ├── schemas/</br>
│   ├── config/</br>
│   │   ├── auth.js</br>
│   │   ├── database.js</br>
│   │   └── multer.js</br>
│   ├── database/</br>
│   │   └── migrations/</br>
│   │       ├── 20240218201527-create-users.js</br>
│   │       ├── 20240221005216-create-products.js</br>
│   │       ├── 20240225183334-create-categories.js</br>
│   │       ├── ...</br>
│   ├── app.js</br>
│   ├── routes.js</br>
│   └── server.js</br>
└── uploads/</br>

## Pré-requisitos

- Docker: Para rodar os containers do PostgreSQL e MongoDB.
- Node.js: Para rodar o projeto localmente e aplicar as migrações.
## Configurações - Banco de dados
- As migrações para o banco de dados estão localizadas no diretório src/database/migrations. Cada arquivo representa uma migração que cria ou altera tabelas no PostgreSQL. As migrações incluem:</br>
- Tabela de usuários com verificação de emails duplicados.
- Tabela de produtos com suporte a uploads de imagem.
- Tabela de categorias para organização dos produtos.

## Configuração dos Contêineres com Docker

Para criar e rodar os contêineres do MongoDB e PostgreSQL, utilize os seguintes comandos:

- Para MongoDB:
```bash</br>
docker run --name mongo -p 27017:27017 -d -t mongo
```
- Para PostgreSQL:
```bash</br>
docker run -d --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=sua-senha -d postgres
```
Após criar o contêiner do PostgreSQL, você pode usar o Postbird para criar o banco de dados necessário e configurar o nome do banco em database.js.

- Executando as Migrações
  
Após configurar o banco de dados, aplique as migrações com o seguinte comando:

yarn sequelize-cli db:migrate

## Comandos para utilizar a aplicação

1- Iniciando o Projeto

- Instale as dependências:
   ```</br>
   npm install
    # ou
   yarn install
2- Iniciando o projento
- Comandos para iniciar o projeto
  ```</br>
  npm run dev
    # ou
  yarn dev
  ```

## Contato
Para mais informações, entre em contato com o desenvolvedor:

Nome: Taylor Reis </br>
Email: taylor-reis@outlook.com </br>
LinkedIn: https://www.linkedin.com/in/taylor--reis/ </br>

> **Status do Projeto**: 🚧 Em Desenvolvimento
