### Laravel Mix and Shopify Theme development
* https://shopify.github.io/themekit/commands/
* https://laravel-mix.com/docs/5.0/installation

```
npm init -y
npm install laravel-mix --save-dev
cp node_modules/laravel-mix/setup/webpack.mix.js ./
```
### webpack.mix.js
```
const mix = require('laravel-mix');

mix.js('src/js/app.js', 'dist')
   .sass('src/scss/app.scss', 'dist')
   .setPublicPath('dist');

mkdir src && touch src/js/app.js && touch src/scss/app.scss
```
### add script package.json
```
"scripts": {
    "dev": "npm run development",
    "development": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
    "watch": "npm run development -- --watch",
    "hot": "cross-env NODE_ENV=development node_modules/webpack-dev-server/bin/webpack-dev-server.js --inline --hot --config=node_modules/laravel-mix/setup/webpack.config.js",
    "prod": "npm run production",
    "production": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --no-progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
}
```
### from command

```
npm install cross-env --save-dev

npm run dev

npm install vue-template-compiler --save-dev

npm run dev

theme watch --allow-live

npm run watch
```
### How to use
* Clone this repo
* Run npm install
* Add config.yml

That's it. Happy coding.
Thanks.
