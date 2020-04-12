![](/img/react-native.png)
<img src="img/1280px-Node.js_logo.svg.png" height="'160" width="300">


# Be The Hero

### Projeto Be The Hero desenvolvido na semana OminiStack 11 - Rocketseat

- Painel web para cadastro das instituições e dos casos.

![](/img/index.png)

![](/img/incidents.png)

- App mobile para acessar os casos e entrar em contato com as instituições.

![](/img/app.jpg)

## Pré-requisitos:
 - Ter o ambiente preparado com nodejs, node, npm, yarn.
 - Git instalado para clonar o projeto.
 - Instalar o expo na máquina e no dispositivo móvel.

### Instalação Expo
Ubuntu:
 ```sh
$ npm install -g expo-cli
```
Instalar o expo no dispositivo móvel:

- [Expo Google Play](https://play.google.com/store/apps/details?id=host.exp.exponent&hl=pt_BR)


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

## Instalação 
Executar o npm install para instalar as dependencias do package.json, criando a pasta node_modules.

O comando abaixo clona o projeto e faz a instalação.
```sh
git clone https://github.com/andersonheinz/react-semanaoministack11-rocketseat && cd react-semanaoministack11-rocketseat/backend && npm i && cd ../frontend && npm i && cd ../mobile && npm i
```
Caso ocorra algum problema, para instalar manualmente é necessário fazer o clone do projeto e dentro das seguintes pastas executar `npm install` :
- backend
- frontend
- mobile

## Executar aplicações

### Backend e Frontend
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

### Mobile
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
