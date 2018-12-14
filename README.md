### bluebird
---
https://github.com/petkaantonov/bluebird/

```
npm install bluebird
```

```js
var Promise = require("bluebird");

import * as Promise from 'bluebird';

var fs = require("fs");
Promise.promisigyAll(fs);
fs.readFileAsync("file.js", "utf8").then(...)

var Promise = require("bluebird");
Promise.promisifyAll(require("redis"));

var Promise = require("bluebird");
Promise.promisifyAll(require('mongodb'));

var Promise = require("bluebird");
Promise.promisifyAll(require("mysql/lib/Connection").prototype);
Promise.promisifyAll(require("mysql/lib/Pool").prototype);

var promise = require("bluebird");
Promise.promisifyAll(require("mongoose"));
```

```
http://bluebirdjs.com/docs/warning-explanations.html
```
