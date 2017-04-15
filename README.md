# api documentation for  [bookshelf (v0.10.3)](http://bookshelfjs.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-bookshelf.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bookshelf) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bookshelf.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bookshelf)
#### A lightweight ORM for PostgreSQL, MySQL, and SQLite3

[![NPM](https://nodei.co/npm/bookshelf.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/bookshelf)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bookshelf/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bookshelf/build/apidoc.html)

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
    "version": "0.10.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module bookshelf](#apidoc.module.bookshelf)
1.  [function <span class="apidocSignatureSpan"></span>bookshelf (knex)](#apidoc.element.bookshelf.bookshelf)
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>initialize (knex)](#apidoc.element.bookshelf.initialize)
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>toString ()](#apidoc.element.bookshelf.toString)



# <a name="apidoc.module.bookshelf"></a>[module bookshelf](#apidoc.module.bookshelf)

#### <a name="apidoc.element.bookshelf.bookshelf"></a>[function <span class="apidocSignatureSpan"></span>bookshelf (knex)](#apidoc.element.bookshelf.bookshelf)
- description and source-code
```javascript
function Bookshelf(knex) {
  var bookshelf = {
    VERSION: require('../package.json').version
  };

  var Model = bookshelf.Model = _model2.default.extend({

    _builder: builderFn,

    // The 'Model' constructor is referenced as a property on the 'Bookshelf'
    // instance, mixing in the correct 'builder' method, as well as the
    // 'relation' method, passing in the correct 'Model' & 'Collection'
    // constructors for later reference.
    _relation: function _relation(type, Target, options) {
      if (type !== 'morphTo' && !(0, _lodash.isFunction)(Target)) {
        throw new Error('A valid target model must be defined for the ' + (0, _lodash.result)(this, 'tableName') + ' ' + type + '
relation');
      }
      return new Relation(type, Target, options);
    }
  }, {

<span class="apidocCodeCommentSpan">    /**
     * @method Model.forge
     * @belongsTo Model
     * @description
     *
     * A simple helper function to instantiate a new Model without needing 'new'.
     *
     * @param {Object=} attributes Initial values for this model's attributes.
     * @param {Object=}  options               Hash of options.
     * @param {string=}  options.tableName     Initial value for {@linkcode Model#tableName tableName}.
     * @param {boolean=} [options.hasTimestamps=false]
     *
     *   Initial value for {@linkcode Model#hasTimestamps hasTimestamps}.
     *
     * @param {boolean} [options.parse=false]
     *
     *   Convert attributes by {@linkcode Model#parse parse} before being
     *   {@linkcode Model#set set} on the 'model'.
     */
</span>    forge: forge,

    /**
     * @method Model.collection
     * @belongsTo Model
     * @description
     *
     * A simple static helper to instantiate a new {@link Collection}, setting
     * the current 'model' as the collection's target.
     *
     * @example
     *
     * Customer.collection().fetch().then(function(collection) {
     *   // ...
     * });
     *
     * @param {(Model[])=} models
     * @param {Object=} options
     * @returns {Collection}
     */
    collection: function collection(models, options) {
      return new bookshelf.Collection(models || [], (0, _lodash.extend)({}, options, { model: this }));
    },


    /**
     * @method Model.count
     * @belongsTo Model
     * @since 0.8.2
     * @description
     *
     * Gets the number of matching records in the database, respecting any
     * previous calls to {@link Model#query query}. If a 'column' is provided,
     * records with a null value in that column will be excluded from the count.
     *
     * @param {string} [column='*']
     *   Specify a column to count - rows with null values in this column will be excluded.
     * @param {Object=} options
     *   Hash of options.
     * @returns {Promise<Number>}
     *   A promise resolving to the number of matching rows.
     */
    count: function count(column, options) {
      return this.forge().count(column, options);
    },


    /**
     * @method Model.fetchAll
     * @belongsTo Model
     * @description
     *
     * Simple helper function for retrieving all instances of the given model.
     *
     * @see Model#fetchAll
     * @returns {Promise<Collection>}
     */
    fetchAll: function fetchAll(options) {
      return this.forge().fetchAll(options);
    }
  });

  var Collection = bookshelf.Collection = _collection2.default.extend({

    _builder: builderFn

  }, {

    /**
     * @method Collection.forge
     * @belongsTo Collection
     * @description
     *
     * A simple helper function to instantiate a new Collection without needing
     * new.
     *
     * @param {(Object[]|Model[])=} [models]
     *   Set of models (or attribute hashes) with which to initialize the
     *   collection.
     * @param {Object} options Hash of options.
     *
     * @example
     *
     * var Promise = require('bluebird');
     * var Accounts = bookshelf.Collection.extend({
     *   model: Account
     * });
     *
     * var accounts = Accounts.forge([
     *   {name: 'Person1'},
     *   {name: 'Person2'}
     * ]);
     *
     * Promise.all(accounts.invoke('save')).then(funct ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bookshelf.initialize"></a>[function <span class="apidocSignatureSpan">bookshelf.</span>initialize (knex)](#apidoc.element.bookshelf.initialize)
- description and source-code
```javascript
initialize = function (knex) {
  _helpers2.default.warn("Bookshelf.initialize is deprecated, pass knex directly: require('bookshelf')(knex)");
  return new Bookshelf(knex);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bookshelf.toString"></a>[function <span class="apidocSignatureSpan">bookshelf.</span>toString ()](#apidoc.element.bookshelf.toString)
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
