# api documentation for  [react-tools (v0.13.3)](https://facebook.github.io/react)  [![npm package](https://img.shields.io/npm/v/npmdoc-react-tools.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-react-tools) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-react-tools.svg)](https://travis-ci.org/npmdoc/node-npmdoc-react-tools)
#### A set of complementary tools to React, including the JSX transformer.

[![NPM](https://nodei.co/npm/react-tools.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-tools)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-tools/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-tools/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-react-tools/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-react-tools/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "jsx": "./bin/jsx"
    },
    "bugs": {
        "url": "https://github.com/facebook/react/issues"
    },
    "commonerConfig": {
        "version": 4
    },
    "dependencies": {
        "commoner": "^0.10.0",
        "jstransform": "^10.1.0"
    },
    "deprecated": "react-tools is deprecated. For more information, visit https://fb.me/react-tools-deprecated",
    "description": "A set of complementary tools to React, including the JSX transformer.",
    "devDependencies": {
        "benchmark": "~1.0.0",
        "browserify": "^9.0.3",
        "bundle-collapser": "^1.1.1",
        "coffee-script": "^1.8.0",
        "coverify": "~1.0.4",
        "derequire": "^2.0.0",
        "envify": "^3.0.0",
        "es3ify": "~0.1.2",
        "es5-shim": "^4.0.0",
        "eslint": "^0.14.1",
        "esprima-fb": "^13001.1001.0-dev-harmony-fb",
        "grunt": "~0.4.2",
        "grunt-cli": "~0.1.9",
        "grunt-compare-size": "~0.4.0",
        "grunt-contrib-clean": "^0.6.0",
        "grunt-contrib-compress": "^0.13.0",
        "grunt-contrib-connect": "~0.6.0",
        "grunt-contrib-jshint": "^0.10.0",
        "grunt-jest": "^0.1.2",
        "gzip-js": "~0.3.2",
        "jasmine-tapreporter": "~0.2.2",
        "jest-cli": "^0.2.1",
        "optimist": "~0.6.0",
        "phantomjs": "~1.9",
        "platform": "^1.1.0",
        "populist": "~0.1.6",
        "recast": "^0.9.11",
        "sauce-tunnel": "~1.1.0",
        "tmp": "~0.0.18",
        "typescript": "^1.4.0",
        "uglify-js": "^2.4.20",
        "uglifyify": "^3.0.1",
        "wd": "~0.2.6"
    },
    "directories": {},
    "dist": {
        "shasum": "da6ac7d4d7777a59a5e951cf46e72fd4b6b40a2c",
        "tarball": "https://registry.npmjs.org/react-tools/-/react-tools-0.13.3.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "files": [
        "main.js",
        "bin/jsx",
        "src/",
        "vendor/fbtransform/",
        "vendor/inline-source-map.js"
    ],
    "homepage": "https://facebook.github.io/react",
    "jest": {
        "rootDir": "",
        "scriptPreprocessor": "jest/preprocessor.js",
        "setupEnvScriptFile": "jest/environment.js",
        "persistModuleRegistryBetweenSpecs": true,
        "testFileExtensions": [
            "js",
            "coffee",
            "ts"
        ],
        "modulePathIgnorePatterns": [
            "/build/",
            "/node_modules/",
            "/.module-cache/"
        ],
        "testPathIgnorePatterns": [
            "/build/",
            "/node_modules/"
        ],
        "unmockedModulePathPatterns": [
            ""
        ]
    },
    "keywords": [
        "react",
        "jsx",
        "transformer",
        "view"
    ],
    "license": "BSD-3-Clause",
    "main": "main.js",
    "maintainers": [
        {
            "name": "zpao"
        },
        {
            "name": "jeffmo"
        }
    ],
    "name": "react-tools",
    "optionalDependencies": {},
    "preferGlobal": true,
    "repository": {
        "type": "git",
        "url": "git+https://github.com/facebook/react.git"
    },
    "scripts": {
        "build": "grunt build",
        "jest": "jest",
        "lint": "eslint src",
        "test": "jest"
    },
    "version": "0.13.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module react-tools](#apidoc.module.react-tools)
1.  [function <span class="apidocSignatureSpan">react-tools.</span>transform (input, options)](#apidoc.element.react-tools.transform)
1.  [function <span class="apidocSignatureSpan">react-tools.</span>transformWithDetails (input, options)](#apidoc.element.react-tools.transformWithDetails)



# <a name="apidoc.module.react-tools"></a>[module react-tools](#apidoc.module.react-tools)

#### <a name="apidoc.element.react-tools.transform"></a>[function <span class="apidocSignatureSpan">react-tools.</span>transform (input, options)](#apidoc.element.react-tools.transform)
- description and source-code
```javascript
transform = function (input, options) {
  options = processOptions(options);
  var output = innerTransform(input, options);
  var result = output.code;
  if (options.sourceMap) {
    var map = inlineSourceMap(
      output.sourceMap,
      input,
      options.filename
    );
    result += '\n' + map;
  }
  return result;
}
```
- example usage
```shell
...
'es6module' | 'true': parses the file as an ES6 module | 'false'
'nonStrictEs6module' | 'true': parses the file as an ES6 module, except disables implicit strict-mode (i.e. CommonJS modules et
al are allowed) | 'false'
'target' | '"es3"': ECMAScript 3<br>'"es5"': ECMAScript 5| '"es5"'

'''js
var reactTools = require('react-tools');

reactTools.transform(string, options);
'''

### 'transformWithDetails(inputString, options)'

Just like 'transform', but outputs an object:
'''js
{
...
```

#### <a name="apidoc.element.react-tools.transformWithDetails"></a>[function <span class="apidocSignatureSpan">react-tools.</span>transformWithDetails (input, options)](#apidoc.element.react-tools.transformWithDetails)
- description and source-code
```javascript
transformWithDetails = function (input, options) {
  options = processOptions(options);
  var output = innerTransform(input, options);
  var result = {};
  result.code = output.code;
  if (options.sourceMap) {
    result.sourceMap = output.sourceMap.toJSON();
  }
  if (options.filename) {
    result.sourceMap.sources = [options.filename];
  }
  return result;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
