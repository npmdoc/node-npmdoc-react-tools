# npmdoc-react-tools

#### basic api documentation for  [react-tools (v0.13.3)](https://facebook.github.io/react)  [![npm package](https://img.shields.io/npm/v/npmdoc-react-tools.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-react-tools) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-react-tools.svg)](https://travis-ci.org/npmdoc/node-npmdoc-react-tools)

#### A set of complementary tools to React, including the JSX transformer.

[![NPM](https://nodei.co/npm/react-tools.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-tools)

- [https://npmdoc.github.io/node-npmdoc-react-tools/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-react-tools/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-tools/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-tools/build/apidoc.html)

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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
