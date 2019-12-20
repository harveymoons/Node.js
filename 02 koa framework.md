 
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
  
###### setup prettierrc
```json
// create [.prettierrc] file on root directory
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
```
  
  
