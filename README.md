# load-appconfig

  A too simple config loader.

## Usage
appconfg.js:
```js
var root = __dirname + '/';

module.exports = {
  appRoot       : root,
  publicDir     : 'public/',
  frontendMain  : 'index.html',
  dbConfigName  : 'dbConfig.js',
  listeningPort : process.env.PORT || '8000'
};
```

app.js:
```js
var config = require('load-appconfig');

var appRoot = config.appRoot;
var dbConfig = require(appRoot + config.dbConfigName);
```

No paths needed to load config.

## Prerequisites
* [Node.js](https://nodejs.org)
* File named appConfig.js in the root of your node app

## Installation

```bash
$ npm install load-appconfig
```

