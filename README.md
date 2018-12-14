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
```
