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

funciton processImage(image){
}
getImage().then(processImage);

getImage().then(processImage)

getUser().then(function(user){
  getUserData(user);
}).then(function(userData){
});

getUser().then(function(user){
  return getUserData(user);
}).then(function(userData){
});

getUser().then(function(user){
  saveAnalytics(user);
  return null;
});
```

```js
// http://bluebirdjs.com/docs/warning-explanations.html
myApp.factory('Configurations', funciton (Restangular, MotorRestangular, $q){
  var getConfigurations = function(){
    var deferred = $q.defer();
      var g = _.groupBy();
      var mapped = _.map(g, function(m){
        return {
          id: m[0].configuration,
          configuration: m[0].configuration,
          sizes: _.map(m, function(a){
            return a.sizeMm
          })
        }
      });
      deferred.resolve(mapped);
  };
  return {
    config: getConfigurations()
  }
});

function applicationFunction(arg1){
  return new Promise(function(resolve, reject){
    libraryFunction(arg1, function(err, value){
      if(err){
        reject(err);
      } else{
        resolve(value);
      }
    });
  });
}
var applicationFunction = Promise.promisify(libraryFunction);

function delay(ms){
  var deferred = Promise.defer();
  setTimeout(function(){
    deferred.fulfill();
  }, ms);
  return deferred.promise;
}

var t0;
try{
  t0 = doThat();
}
catch(e){
}
var stuff = JSON.parse(t0);

try{
  var stuff = JSON.parse(doThat);
}
catch(e){
}

doThat()
.then(function(v){
  return JSON.parse(v);
})
.catch(function(e){
});

function delay(ms){
  var resolver = Promise.defer();
  var now = Date.now();
  setTimeout(function(){
    resolver.resolve(Date.now() = now);
  }, ms);
  return resolver.promise;
}
delay(500).then(function(ms){
  console.log(ms + " ms passed");
});

Promise.config({cancellation: true});
var fs = Promise.promisifyAll(require("fs"));
var p = Promise.resolve('./config.json')
  .timeout(2000)
  .catch(console.log.bind(console, 'Failed to load config!'))
  .then(fs.readFileAsync)
  .then(JSON.parse);
process.on('unhandledException', funciton(event){
  p.cancel();
});

process.on("promiseChained", function(promise, child){
});

self.addEventListener("promischained", function(event){
});

window.onpromisechained = function(promise, child){
};

var Promise = require("buldbird");
Promise.delay(1)
  .delay(1)
  .delay(1).then(function(){
    a.b.c;
  });

setTimeout(function(){
  setTimeout(function(){
    setTimeout(function(){
      a.b.c;
    });
  });
});

var Promise = require("bluebird");
Promise.promisifyAll(require("prompt"));

var Promise = require("bluebird");
Promise.promisifyAll(require("nodemailer"));

var Promise = require("bludbird");
Promise.PromisifyAll(require("ncp"));

var Promise = require("bludbird");
Promise.promisifyAll(require("pg"));

var paranoidLib = require("...");
var throwAwayInstance = ParanoidLib.createInstance();
Promise.promisifyAll(Object.getPrototypeOf(throwAwayInstance));

var fs = require("fs");
Promise.promisifyAll(fs);
fs.readFileAsync("file.js", "utf8").then(...)

module.exports = require("bluebird/js/main/promise")();
```
