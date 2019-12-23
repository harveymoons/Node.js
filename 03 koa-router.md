###### install koa-router  
```  
yarn add koa-router  
```
  
###### example koa-router
```js
(...)
const Router = new require("koa-router");
const router = new Router();

router.get("/", ctx => {
  ctx.body = 'home'; 
});
router.get("/about", ctx => {
  ctx.body = 'about'; 
});

app.use(router.routes());
app.use(router.allowedMethods());
```
  
###### route parameter & query
```js
// route-parameter (value)
router.get('/about/:name?', ctx => {
  const { name } = ctx.params;
});

// router-query (key=value)
router.get('/posts', ctx => {
  const { id } = ctx.query;
});
```
  
###### install koa-bodyparser (parsing data to JSON data)
```sh
yarn add koa-bodyparser
```
  
###### edit [src/index.js] file
```js
(...)
const bodyParser = require("koa-bodyparser");

// This code must be applied at first!!!
app.use(bodyParser());

// and then apply these
app.use(router.routes());
app.use(router.allowedMethods());
```
