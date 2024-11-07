# Intégration de maquette en SASS avec webpack

## Installation

- Clonage de ce dépôt git 
```shell 
git clone https://github.com/adrienm94/Maquette-Lilipinso-SASS.git
```
- Se placer dans le répertoire créé **Maquette-Lilipinso-SASS**
```shell
cd Maquette-Lilipinso-SASS
```
- Initilisation du projet avec node package manager fourni par ([NodeJS](https://nodejs.org/))
```shell
npm init -y
```
- Installation de webpack en mode développement:
```shell
npm install webpack webpack-cli --save-dev
```
- Installation des loaders:
```shell
npm install html-loader sass-loader css-loader style-loader sass --save-dev
```
- Installation du plugin HtmlWebPackPlugin pour la création simplifiée de fichiers html:
```shell
npm install html-webpack-plugin --save-dev
```
- Installation du serveur de développement :
```shell
npm install webpack-dev-server --save-dev
```
- Création d'un fichier de configuration ([**webpack.config.json**](https://github.com/adrienm94/Maquette-Lilipinso-SASS/blob/main/webpack.config.js))

- Le fichier package.json :
```json
{
  "name": "tp-adrien-meyrand",
  "version": "1.0.0",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack-dev-server",
    "build": "NODE_ENV=production webpack"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "devDependencies": {
    "css-loader": "^7.1.2",
    "html-loader": "^5.1.0",
    "html-webpack-plugin": "^5.6.0",
    "image-loader": "^0.0.1",
    "image-webpack-loader": "^8.1.0",
    "sass": "^1.79.3",
    "sass-loader": "^16.0.2",
    "style-loader": "^4.0.0",
    "webpack": "^5.95.0",
    "webpack-cli": "^5.1.4",
    "webpack-dev-server": "^5.1.0"
  }
}
 ```
- Pour lancer le serveur de développement sur le port 8080 :
```shell
npm start
```







 
