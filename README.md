require-many
============

Import an array of node modules, using globbing and require.resolve.
```js
const requireMany = require('require-many');

const locals = requireMany('./services/*.js'); // if you start with ./ they are local modules

const abs = requireMany('/home/sithmel/services/*.js'); // if you start with / they are absolute urls

const decorators = requireMany('async-deco/src/*.js'); // in this case it will resolve from the package "async-deco"

const decorators = requireMany(['./services/*.js', 'module1/services/*.js']); // you can use an array to include multiple globs
```
