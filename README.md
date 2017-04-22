# npmdoc-bookshelf

#### api documentation for  [bookshelf (v0.10.3)](http://bookshelfjs.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-bookshelf.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bookshelf) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bookshelf.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bookshelf)

#### A lightweight ORM for PostgreSQL, MySQL, and SQLite3

[![NPM](https://nodei.co/npm/bookshelf.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/bookshelf)

- [https://npmdoc.github.io/node-npmdoc-bookshelf/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-bookshelf/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bookshelf/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bookshelf/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-bookshelf/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-bookshelf/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tim Griesser",
        "url": "https://github.com/tgriesser"
    },
    "bugs": {
        "url": "https://github.com/tgriesser/bookshelf/issues"
    },
    "buildDependencies": [
        "babel-cli",
        "babel-runtime",
        "babel-plugin-syntax-object-rest-spread",
        "babel-plugin-transform-object-rest-spread",
        "babel-plugin-transform-runtime",
        "babel-preset-es2015"
    ],
    "dependencies": {
        "babel-runtime": "^6.6.1",
        "bluebird": "^3.4.3",
        "chalk": "^1.0.0",
        "create-error": "~0.3.1",
        "inflection": "^1.5.1",
        "inherits": "~2.0.1",
        "lodash": "^4.13.1"
    },
    "description": "A lightweight ORM for PostgreSQL, MySQL, and SQLite3",
    "devDependencies": {
        "babel-cli": "^6.0.15",
        "babel-eslint": "^6.1.2",
        "babel-plugin-syntax-object-rest-spread": "^6.0.14",
        "babel-plugin-transform-object-rest-spread": "^6.0.14",
        "babel-plugin-transform-runtime": "^6.6.0",
        "babel-preset-es2015": "^6.0.14",
        "bookshelf-jsdoc-theme": "^0.1.2",
        "chai": "^3.5.0",
        "eslint": "2.13.1",
        "istanbul": "^0.4.5",
        "jsdoc": "^3.4.0",
        "knex": "^0.12.0",
        "minimist": "^1.1.0",
        "mocha": "^3.0.2",
        "mysql": "^2.5.2",
        "node-uuid": "~1.4.1",
        "pg": "^6.1.0",
        "semver": "^5.0.3",
        "sinon": "^1.11.1",
        "sinon-chai": "^2.6.0",
        "sqlite3": "^3.0.5"
    },
    "directories": {},
    "dist": {
        "shasum": "72558204e83815f8e5bba6fd808702563e72b3e4",
        "tarball": "https://registry.npmjs.org/bookshelf/-/bookshelf-0.10.3.tgz"
    },
    "gitHead": "06bdd009805cd6be83c002fd3a114e8ddb4e907a",
    "homepage": "http://bookshelfjs.org",
    "keywords": [
        "orm",
        "mysql",
        "postgresql",
        "sqlite",
        "datamapper",
        "active record"
    ],
    "license": "MIT",
    "main": "bookshelf.js",
    "maintainers": [
        {
            "name": "erisds"
        },
        {
            "name": "kirrg001"
        },
        {
            "name": "rhys-vdw"
        },
        {
            "name": "tgriesser"
        }
    ],
    "name": "bookshelf",
    "optionalDependencies": {},
    "peerDependencies": {
        "knex": ">=0.6.10 <0.13.0"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/tgriesser/bookshelf.git"
    },
    "scripts": {
        "build": "babel -q -L -D ./src/ --out-dir ./lib/",
        "clean": "rm -rf ./lib",
        "cover": "npm run lint && istanbul cover _mocha -- --check-leaks -t 10000 -b -R spec test/index.js",
        "dev": "babel -w -q -L -D ./src/ --out-dir ./lib/",
        "gh-pages": "./scripts/gh-pages.sh",
        "jsdoc": "./scripts/jsdoc.sh",
        "lint": "eslint bookshelf.js src/",
        "postinstall": "node ./scripts/build.js lib \"npm run build\"",
        "postpublish": "./scripts/postpublish.sh",
        "prepublish": "npm run build",
        "test": "npm run lint &&  mocha --check-leaks -t 10000 -b test/index.js"
    },
    "version": "0.10.3",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
