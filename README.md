# api documentation for  log (v1.4.0)  [![npm package](https://img.shields.io/npm/v/npmdoc-log.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-log) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-log.svg)](https://travis-ci.org/npmdoc/node-npmdoc-log)
#### Tiny logger with streaming reader

[![NPM](https://nodei.co/npm/log.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/log)

[![apidoc](https://npmdoc.github.io/node-npmdoc-log/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-log/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-log/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-log/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk"
    },
    "dependencies": {},
    "description": "Tiny logger with streaming reader",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "4ba1d890fde249b031dca03bc37eaaf325656f1c",
        "tarball": "https://registry.npmjs.org/log/-/log-1.4.0.tgz"
    },
    "engines": {
        "node": ">= 0.2.0"
    },
    "keywords": [
        "log",
        "logger"
    ],
    "main": "./lib/log.js",
    "maintainers": [
        {
            "name": "tjholowaychuk"
        }
    ],
    "name": "log",
    "optionalDependencies": {},
    "version": "1.4.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module log](#apidoc.module.log)
1.  [function <span class="apidocSignatureSpan"></span>log (level, stream)](#apidoc.element.log.log)
1.  [function <span class="apidocSignatureSpan">log.</span>toString ()](#apidoc.element.log.toString)
1.  number <span class="apidocSignatureSpan">log.</span>ALERT
1.  number <span class="apidocSignatureSpan">log.</span>CRITICAL
1.  number <span class="apidocSignatureSpan">log.</span>DEBUG
1.  number <span class="apidocSignatureSpan">log.</span>EMERGENCY
1.  number <span class="apidocSignatureSpan">log.</span>ERROR
1.  number <span class="apidocSignatureSpan">log.</span>INFO
1.  number <span class="apidocSignatureSpan">log.</span>NOTICE
1.  number <span class="apidocSignatureSpan">log.</span>WARNING



# <a name="apidoc.module.log"></a>[module log](#apidoc.module.log)

#### <a name="apidoc.element.log.log"></a>[function <span class="apidocSignatureSpan"></span>log (level, stream)](#apidoc.element.log.log)
- description and source-code
```javascript
function Log(level, stream){
  if ('string' == typeof level) level = exports[level.toUpperCase()];
  this.level = level || exports.DEBUG;
  this.stream = stream || process.stdout;
  if (this.stream.readable) this.read();
}
```
- example usage
```shell
...
     , log = new Log('debug', fs.createWriteStream('my.log'));

Instead of the log level constants, you may also supply a string:

   var Log = require('log')
     , log = new Log('warning');

We can also use '%s' much like 'console.log()' to pass arguments:

    log.error('oh no, failed to send mail to %s.', user.email);

## Reader

To stream a log, simply pass a readable stream instead of a writable:
...
```

#### <a name="apidoc.element.log.toString"></a>[function <span class="apidocSignatureSpan">log.</span>toString ()](#apidoc.element.log.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
