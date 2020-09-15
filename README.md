# Covid Tracker

## Proposta

[Desafio LATITUDE](https://gitlab.com/GuiFay/selecao-latitude/-/blob/master/README.md)

### Funcionalidade

A proposta é um **cadastro de pessoas com COVID-19**.

O usuário poderá:

- Cadastrar suas informações no site (**obrigatório**);
- Ver informações de outros usuários (**obrigatório**).

### Tecnologia

A aplicação SPA (_Angular pref._) deverá consumir uma API local (_Java Spring pref._) e guardar as infos em um banco de dados (_PostreSQL pref._).

**Frontend**
- Tela de cadastro com nome e endereço, no mínimo (**obrigatório**);
- Tabela de pessoas cadastradas (**obrigatório**).

**Backend (API Rest)**
- POST para cadastro;
- GET para buscar cadastrados.

**Bônus**
- Validação dos campos;
- Máscara nos campos;
- Mostrar ponto no mapa com os cadastrados;
- Docker-compose para subir as duas aplicações;
- Integração contínua do GitLab;
- Teste automatizado para validar o CI;

**Outras ideias**
- Salvar perfis nos cookies para mais de um usuário por dispositivo;
- Mapa com agrupamento de acordo com o zoom;
- Informação por pessoas dentro de 1km de vocês;
- Tema dark;
- Esconder nome;


### Referências
**Guardiões da Saúde**

- Cadastro
  - Nome, gênero, raça, nascimento, origem, cidade, estado, país, grupo de risco.
- Como está se sentindo no dia;
- Acompanhamento no calendário;
- Mapa diário com o estado e a localização das pessoas;
- Dicas;
- Notícias.


### Plan workflow

### Wireframe

### Seek validation

### Database

### Frontend

### Backend

### Docker or Host

### Deploy

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
