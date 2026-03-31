# Intégration de maquette en SASS avec webpack

## Récupération du code

- Clonage de ce dépôt git 
```shell 
git clone https://github.com/adrienm94/Maquette-Lilipinso-SASS.git
```
- Se placer dans le répertoire créé **Maquette-Lilipinso-SASS**
```shell
cd Maquette-Lilipinso-SASS
```

## Installation des dépendances nécessaires en mode développement

- Utilisation nécessire de npm (node package manager) fourni par ([NodeJS](https://nodejs.org/))
- Installation de webpack :
```shell
npm install webpack webpack-cli --save-dev
```
- Installation des loaders :
```shell
npm install html-loader sass-loader css-loader style-loader sass --save-dev
```
- Installation du plugin HtmlWebPackPlugin pour la création simplifiée de fichiers html :
```shell
npm install html-webpack-plugin --save-dev
```
- Installation du serveur de développement :
```shell
npm install webpack-dev-server --save-dev
```
- Le fichier de configuration webpack.config.js :
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
    entry: './src/main.js', // Le fichier js principale de notre code source.
    mode: 'development',
    output: {
        filename: 'main.js', // Le nom du bundle à générer
        path: path.resolve(__dirname, 'dist'), // Le chemin dans lequel le bundle doit être généré
    },
    module: {
        rules: [
            {
                test: /.scss$/,
                use: ["style-loader", "css-loader", "sass-loader"],
            },
            {
                test: /\.html$/i,
                loader: "html-loader",
            }
        ],
    },
    plugins: [new HtmlWebpackPlugin({
        template: 'src/index.html'
    })]
};
```

- Pour lancer le serveur de développement sur le port 8080 :
```shell
npm start
```







 
