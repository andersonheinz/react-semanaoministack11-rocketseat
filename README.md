

<h1 align="center">
<img alt="Be The Hero" src="frontend/src/assets/logo.svg" height="'130" width="200px">
</h1>


<h4 align="center">
  🚀 Semana OmniStack 11.0
</h4>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/andersonheinz/react-semanaoministack11-rocketseat">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/andersonheinz/react-semanaoministack11-rocketseat">
  
  <a href="https://github.com/Rocketseat/semana-omnistack-10/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/andersonheinz/react-semanaoministack11-rocketseat">
  </a>

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-red">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-brightgreen">
</p>

<p align="center">
  <a href="#rocket-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#octocat-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <a href="#-web-demo">Demo</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#anger-pr%C3%A9-requisitos">Pré Requisitos</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#wrench-instala%C3%A7%C3%A3o">Instalação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>


## 🚀 Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- [Node.js](https://nodejs.org/en/)
- [React](https://reactjs.org)
- [React Native](https://facebook.github.io/react-native/)
- [Expo](https://expo.io/)


## :octocat: Projeto
Be the Hero é um projeto que visa ajudar instituições sem fins lucrativos, o cadastro das instituições é feito na web, através do app as pessoas podem entrar em contato para fazerem doações e ajudar em determinada causa!

## 💻 Web Demo

![](/img/index.png)

![](/img/incidents.png)

## 📱 App Demo

App mobile para acessar os casos e entrar em contato com as instituições.

![](/img/app.jpg)

## :anger: Pré-requisitos:
 - Ter o ambiente preparado com nodejs, node, npm, yarn.
 - Git instalado para clonar o projeto.
 - Instalar o expo na máquina e no dispositivo móvel.

### Verificar instalação/ versões utilizadas
Verificar se os requisitos estão instalados, não é necessário utilizar as versões especificadas abaixo, porém no momento que foi criado esse projeto, essas são as versões do ambiente:
```sh
$ node -v  
v12.16.1

$ npm -v   
6.13.4

$ nodejs -v
v10.19.0

$ yarn -v   
1.22.4

$ expo --version
3.17.23
```

## :wrench: Instalação 

### Instalação Expo
Ubuntu:
 ```sh
$ npm install -g expo-cli
```
Instalar o expo no dispositivo móvel:

- [Expo Google Play](https://play.google.com/store/apps/details?id=host.exp.exponent&hl=pt_BR)

<br>

Executar o npm install para instalar as dependencias do package.json, criando a pasta node_modules.

O comando abaixo clona o projeto e faz a instalação.
```sh
git clone https://github.com/andersonheinz/react-semanaoministack11-rocketseat && cd react-semanaoministack11-rocketseat/backend && npm i && cd ../frontend && npm i && cd ../mobile && npm i
```
Caso ocorra algum problema, para instalar manualmente é necessário fazer o clone do projeto e dentro das pastas backend, frontend e mobile, executar `npm install` para instalar as dependencias do package.json, criando a pasta node_modules.

### Executar aplicações Backend e Frontend

- Abrir terminal na pasta backend e executar `npm start`
- Abrir nova aba no terminal na pasta frontend e executar `npm start`

O comando `npm start` executa os scripts informados no arquivo `package.json`. No backend foi configurado para executar o projeto através do nodemon:
```sh
"scripts": {"start": "nodemon src/server.js"},
```

> O Nodemon é um utilitário que monitora qualquer alteração na sua fonte e reinicia automaticamente o servidor.

#### Verificar se os backend e frontend estão funcionando.

Listar o JSON das ONG's cadastradas
http://localhost:3333/ongs

Página index da aplicação web
http://localhost:3000/

### Executar aplicação Mobile
- Alterar o IP da baseURL no arquivo react-semanaoministack11-rocketseat/mobile/src/services/api.js

```sh
const api = axios.create({
  baseURL: 'http://192.168.X.XXX:3333'
});
```
Para iniciar a aplicação mobile executar yarn start, expo start ou npm start.

```sh
$ expo start
```
> Com o expo não é necessário instalar o Sdk do Android ou o XCode para MAC.

Irá abrir no navegador a página do expo. 

Abrir o app do Expo instalado no dispositivo móvel, escanear o QR Code do navegador, e estará pronto para uso.


Se o app não carregar e aparecer "could not load... timeout" será necessario desabilitar o firewall, e executar novamente o expo start e escanear o QR Code.
```sh
$ sudo ufw disable
```

### :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.
