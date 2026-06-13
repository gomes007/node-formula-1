# Node Formula 1 API

Projeto desenvolvido como parte do desafio prático da DIO, com o objetivo de praticar conceitos de **Node.js**, **TypeScript**, **Fastify**, rotas HTTP, scripts npm e organização de projetos backend.

A aplicação consiste em uma API simples sobre Fórmula 1, permitindo consultar equipes e pilotos.

## Tecnologias Utilizadas

* Node.js
* TypeScript
* Fastify
* @fastify/cors
* TSX
* TSUP
* NPM

## Funcionalidades

A API possui as seguintes rotas:

### Listar equipes

```http
GET /teams
```

Retorna a lista de equipes de Fórmula 1 cadastradas.

### Buscar equipe por ID

```http
GET /teams/:id
```

Retorna uma equipe específica pelo seu ID.

Exemplo:

```http
GET /teams/4
```

### Listar pilotos

```http
GET /drivers
```

Retorna a lista de pilotos cadastrados.

### Buscar piloto por ID

```http
GET /drivers/:id
```

Retorna um piloto específico pelo seu ID.

Exemplo:

```http
GET /drivers/1
```

## Melhorias Implementadas

Além de executar o projeto original, realizei uma melhoria na API:

* Correção do ID duplicado na lista de pilotos.
* Criação da rota `GET /teams/:id` para buscar uma equipe específica pelo ID.
* Tratamento de erro para quando uma equipe não for encontrada.

Exemplo de retorno quando a equipe não existe:

```json
{
  "message": "Team Not Found"
}
```

## Como Executar o Projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/gomes007/node-formula-1.git
```

### 2. Acessar a pasta do projeto

```bash
cd node-formula-1
```

### 3. Instalar as dependências

```bash
npm install
```

### 4. Executar em modo desenvolvimento

```bash
npm run start:dev
```

A aplicação será iniciada em:

```http
http://localhost:3333
```

## Scripts Disponíveis

```bash
npm run start:dev
```

Executa o projeto em modo desenvolvimento.

```bash
npm run start:watch
```

Executa o projeto em modo desenvolvimento com recarregamento automático.

```bash
npm run dist
```

Compila os arquivos TypeScript para JavaScript na pasta `dist`.

```bash
npm run start:dist
```

Executa a versão compilada do projeto.

## Exemplos de Teste

Após iniciar o servidor, acesse no navegador ou em uma ferramenta como Postman/Insomnia:

```http
http://localhost:3333/teams
```

```http
http://localhost:3333/teams/4
```

```http
http://localhost:3333/drivers
```

```http
http://localhost:3333/drivers/1
```

## Aprendizados

Neste projeto, pratiquei:

* Criação de API com Node.js e Fastify.
* Uso de TypeScript em aplicações backend.
* Criação de rotas HTTP.
* Manipulação de parâmetros de rota.
* Retorno de respostas em JSON.
* Tratamento básico de erros.
* Execução de scripts npm.
* Documentação de projeto no GitHub.

## Referência

Projeto original da DIO:

```text
https://github.com/digitalinnovationone/node-formula-1
```
