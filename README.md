# npmdoc-dot

#### api documentation for  [dot (v1.1.1)](http://github.com/olado/doT)  [![npm package](https://img.shields.io/npm/v/npmdoc-dot.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-dot) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-dot.svg)](https://travis-ci.org/npmdoc/node-npmdoc-dot)

#### Concise and fast javascript templating compatible with nodejs and other javascript environments

[![NPM](https://nodei.co/npm/dot.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/dot)

- [https://npmdoc.github.io/node-npmdoc-dot/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-dot/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dot/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dot/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-dot/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-dot/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Laura Doktorova"
    },
    "bin": {
        "dottojs": "./bin/dot-packer"
    },
    "bugs": {
        "url": "https://github.com/olado/doT/issues"
    },
    "dependencies": {},
    "description": "Concise and fast javascript templating compatible with nodejs and other javascript environments",
    "devDependencies": {
        "commander": "*",
        "coveralls": "^2.11.14",
        "eslint": "^3.9.1",
        "if-node-version": "^1.1.0",
        "jshint": "*",
        "mkdirp": "*",
        "mocha": "*",
        "nyc": "^8.3.2",
        "pre-commit": "^1.1.3",
        "uglify-js": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "1aa26a12b38b1dcccb496714a44303b72efd9ac0",
        "tarball": "https://registry.npmjs.org/dot/-/dot-1.1.1.tgz"
    },
    "engines": [
        "node >=0.2.6"
    ],
    "gitHead": "90edb5d9e75ed7e26341ff3b4de4dcfc3ee54c4f",
    "homepage": "http://github.com/olado/doT",
    "keywords": [
        "template",
        "fast",
        "simple",
        "templating"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "esp"
        },
        {
            "name": "olado"
        }
    ],
    "name": "dot",
    "nyc": {
        "exclude": [
            "test",
            "node_modules"
        ],
        "reporter": [
            "lcov",
            "text-summary"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/olado/doT.git"
    },
    "scripts": {
        "bundle": "uglifyjs doT.js -o doT.min.js -c -m --preamble '/* Laura Doktorova https://github.com/olado/doT */'",
        "eslint": "if-node-version '>=4' eslint *.js --ignore-pattern *.min.js",
        "prepublish": "npm run bundle",
        "test": "npm run eslint && npm run test-cov",
        "test-cov": "nyc mocha test/*.test.js"
    },
    "version": "1.1.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
