require-node-glob
=================
Yet another require-all variant. Sadly I didn't find one that:
* works for relative/absolute urls
* works for modules
* returning an array

Import an array of node modules, using globbing and require.resolve.
```js
const requireGlob = require('require-node-glob');

const locals = requireGlob('./services/*.js'); // if you start with ./ they are local modules

const abs = requireGlob('/home/sithmel/services/*.js'); // if you start with / they are absolute urls

const decorators = requireGlob('async-deco/src/*.js'); // in this case it will resolve from the package "async-deco"

const decorators = requireGlob(['./services/*.js', 'module1/services/*.js']); // you can use an array to include multiple globs
```
