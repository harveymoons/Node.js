 
## Config Project

- **nvm** : node version manager
- **npm** : node package manager
- **yarn** : javaScript package manager
- **nodejs** : backend js language on V8(Google)
  
###### check node/npm version
```sh
node -v
npm -v
```
  
###### install yarn && check version
```sh
npm install -g yarn
yarn -v
```
  
###### create koa project
```sh
mkdir koa-project
cd koa-project
yarn init
yarn add koa
```
  
###### setup ESLint (check javaScript syntax) plugin
```sh
npm install -g eslint
eslint -v
eslint --init # on project root directory
```
  
###### create [.prettierrc] file on root directory
```json
{
  "singleQuote": true,
  "semi": true,
  "useTabs": false,
  "tabWidth": "2",
  "trailingComma": "all",
  "printWidth": 80
}
```
  
###### create eslint-config-prettier
```sh
# prevent conflict between eslint-config to prettier-config
yarn add eslint-config-prettier
```
  
###### edit .eslintrc.json file
```json
(...)
"extends": ["eslint:recommended", "plugin:vue/essential", "prettier"],
(...)
"rules": {
  "no-unused-vars": "warn",
  "no-console": "warn"
}
(...)
```
  
###### create src directory && index.js file
```
mkdir src
cd src
touch index.js
```
  
###### type server code
```js
const Koa = require('koa');
const app = new Koa();

app.use(ctx => {
    ctx.body = 'Hello Koa';
});

app.listen(4000, () => {
    console.log('heurm server is listening to port 4000');
});
```
  
###### run server
```sh
node src # [/index.js]
```
  
###### install nodemon (server restart automatically when code has been changed)
```
yarn add --dev nodemon
```
  
###### edit [package.json] file
```json
(...)
"start": "node src",
"start:dev": "nodemon --watch src/ src/index.js"
(...)    
```
 
