# api documentation for  [bookshelf (v0.10.3)](http://bookshelfjs.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-bookshelf.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bookshelf) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bookshelf.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bookshelf)
#### A lightweight ORM for PostgreSQL, MySQL, and SQLite3

[![NPM](https://nodei.co/npm/bookshelf.png?downloads=true)](https://www.npmjs.com/package/bookshelf)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bookshelf/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-bookshelf_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bookshelf/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-bookshelf/build/screen-capture.npmPackageListing.svg)



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
            "name": "erisds",
            "email": "erisds@gmail.com"
        },
        {
            "name": "kirrg001",
            "email": "katharina.irrgang@googlemail.com"
        },
        {
            "name": "rhys-vdw",
            "email": "rhys.vdw@gmail.com"
        },
        {
            "name": "tgriesser",
            "email": "tgriesser10@gmail.com"
        }
    ],
    "name": "bookshelf",
    "optionalDependencies": {},
    "peerDependencies": {
        "knex": ">=0.6.10 <0.13.0"
    },
    "readme": "ERROR: No README data found!",
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
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>initialize (knex)](#apidoc.element.bookshelf.initialize)
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>model ()](#apidoc.element.bookshelf.model)
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>sync (syncing, options)](#apidoc.element.bookshelf.sync)
1.  object <span class="apidocSignatureSpan">bookshelf.</span>collection
1.  object <span class="apidocSignatureSpan">bookshelf.</span>eager
1.  object <span class="apidocSignatureSpan">bookshelf.</span>errors
1.  object <span class="apidocSignatureSpan">bookshelf.</span>helpers
1.  object <span class="apidocSignatureSpan">bookshelf.</span>model.prototype
1.  object <span class="apidocSignatureSpan">bookshelf.</span>relation
1.  object <span class="apidocSignatureSpan">bookshelf.</span>sync.prototype

#### [module bookshelf.collection](#apidoc.module.bookshelf.collection)
1.  [function <span class="apidocSignatureSpan">bookshelf.collection.</span>default ()](#apidoc.element.bookshelf.collection.default)

#### [module bookshelf.eager](#apidoc.module.bookshelf.eager)
1.  [function <span class="apidocSignatureSpan">bookshelf.eager.</span>default ()](#apidoc.element.bookshelf.eager.default)

#### [module bookshelf.errors](#apidoc.module.bookshelf.errors)
1.  [function <span class="apidocSignatureSpan">bookshelf.errors.</span>EmptyError (message, obj)](#apidoc.element.bookshelf.errors.EmptyError)
1.  [function <span class="apidocSignatureSpan">bookshelf.errors.</span>NoRowsDeletedError (message, obj)](#apidoc.element.bookshelf.errors.NoRowsDeletedError)
1.  [function <span class="apidocSignatureSpan">bookshelf.errors.</span>NoRowsUpdatedError (message, obj)](#apidoc.element.bookshelf.errors.NoRowsUpdatedError)
1.  [function <span class="apidocSignatureSpan">bookshelf.errors.</span>NotFoundError (message, obj)](#apidoc.element.bookshelf.errors.NotFoundError)

#### [module bookshelf.helpers](#apidoc.module.bookshelf.helpers)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>deprecate (a, b)](#apidoc.element.bookshelf.helpers.deprecate)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>error (msg)](#apidoc.element.bookshelf.helpers.error)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>morphCandidate (candidates, foreignTable)](#apidoc.element.bookshelf.helpers.morphCandidate)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>orderBy (obj, sort, order)](#apidoc.element.bookshelf.helpers.orderBy)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>query (obj, args)](#apidoc.element.bookshelf.helpers.query)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>saveConstraints (model, relatedData)](#apidoc.element.bookshelf.helpers.saveConstraints)
1.  [function <span class="apidocSignatureSpan">bookshelf.helpers.</span>warn (msg)](#apidoc.element.bookshelf.helpers.warn)

#### [module bookshelf.model](#apidoc.module.bookshelf.model)
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>model ()](#apidoc.element.bookshelf.model.model)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.</span>NoRowsDeletedError (message, obj)](#apidoc.element.bookshelf.model.NoRowsDeletedError)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.</span>NoRowsUpdatedError (message, obj)](#apidoc.element.bookshelf.model.NoRowsUpdatedError)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.</span>NotFoundError (message, obj)](#apidoc.element.bookshelf.model.NotFoundError)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.</span>extend (protoProps, staticProps)](#apidoc.element.bookshelf.model.extend)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.</span>extended (child)](#apidoc.element.bookshelf.model.extended)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.</span>super_ ()](#apidoc.element.bookshelf.model.super_)
1.  object <span class="apidocSignatureSpan">bookshelf.model.</span>__super__

#### [module bookshelf.model.prototype](#apidoc.module.bookshelf.model.prototype)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_doFetch ()](#apidoc.element.bookshelf.model.prototype._doFetch)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_handleEager (response, options)](#apidoc.element.bookshelf.model.prototype._handleEager)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_handleResponse (response)](#apidoc.element.bookshelf.model.prototype._handleResponse)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_morphOneOrMany (Target, morphName, columnNames, morphValue, type)](#apidoc.element.bookshelf.model.prototype._morphOneOrMany)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>all ()](#apidoc.element.bookshelf.model.prototype.all)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>belongsTo (Target, foreignKey, foreignKeyTarget)](#apidoc.element.bookshelf.model.prototype.belongsTo)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>belongsToMany (Target, joinTableName, foreignKey, otherKey, foreignKeyTarget, otherKeyTarget)](#apidoc.element.bookshelf.model.prototype.belongsToMany)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>clone ()](#apidoc.element.bookshelf.model.prototype.clone)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>count (column, options)](#apidoc.element.bookshelf.model.prototype.count)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>destroy ()](#apidoc.element.bookshelf.model.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>fetch (options)](#apidoc.element.bookshelf.model.prototype.fetch)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>fetchAll (options)](#apidoc.element.bookshelf.model.prototype.fetchAll)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>hasMany (Target, foreignKey, foreignKeyTarget)](#apidoc.element.bookshelf.model.prototype.hasMany)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>hasOne (Target, foreignKey, foreignKeyTarget)](#apidoc.element.bookshelf.model.prototype.hasOne)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>load ()](#apidoc.element.bookshelf.model.prototype.load)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>morphMany (Target, name, columnNames, morphValue)](#apidoc.element.bookshelf.model.prototype.morphMany)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>morphOne (Target, name, columnNames, morphValue)](#apidoc.element.bookshelf.model.prototype.morphOne)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>morphTo (morphName)](#apidoc.element.bookshelf.model.prototype.morphTo)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>orderBy ()](#apidoc.element.bookshelf.model.prototype.orderBy)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>query ()](#apidoc.element.bookshelf.model.prototype.query)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>refresh (options)](#apidoc.element.bookshelf.model.prototype.refresh)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>resetQuery ()](#apidoc.element.bookshelf.model.prototype.resetQuery)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>save ()](#apidoc.element.bookshelf.model.prototype.save)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>sync (options)](#apidoc.element.bookshelf.model.prototype.sync)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>through (Interim, throughForeignKey, otherKey, throughForeignKeyTarget, otherKeyTarget)](#apidoc.element.bookshelf.model.prototype.through)
1.  [function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>where ()](#apidoc.element.bookshelf.model.prototype.where)

#### [module bookshelf.relation](#apidoc.module.bookshelf.relation)
1.  [function <span class="apidocSignatureSpan">bookshelf.relation.</span>default ()](#apidoc.element.bookshelf.relation.default)

#### [module bookshelf.sync](#apidoc.module.bookshelf.sync)
1.  [function <span class="apidocSignatureSpan">bookshelf.</span>sync (syncing, options)](#apidoc.element.bookshelf.sync.sync)

#### [module bookshelf.sync.prototype](#apidoc.module.bookshelf.sync.prototype)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>count ()](#apidoc.element.bookshelf.sync.prototype.count)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>del ()](#apidoc.element.bookshelf.sync.prototype.del)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>first ()](#apidoc.element.bookshelf.sync.prototype.first)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>insert ()](#apidoc.element.bookshelf.sync.prototype.insert)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>prefixFields (fields)](#apidoc.element.bookshelf.sync.prototype.prefixFields)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>select ()](#apidoc.element.bookshelf.sync.prototype.select)
1.  [function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>update ()](#apidoc.element.bookshelf.sync.prototype.update)



# <a name="apidoc.module.bookshelf"></a>[module bookshelf](#apidoc.module.bookshelf)

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

#### <a name="apidoc.element.bookshelf.model"></a>[function <span class="apidocSignatureSpan">bookshelf.</span>model ()](#apidoc.element.bookshelf.model)
- description and source-code
```javascript
model = function () {
  return Parent.apply(this, arguments);
}
```
- example usage
```shell
...
 *  Optionally run the query in a transaction.
 *
 * @throws {Model.NotFoundError}
 * @returns {Promise<Model|null>}
 *  A promise resolving to the fetched {@link Model model} or 'null' if none exists.
 */
fetchOne: _promise2.default.method(function (options) {
  var model = new this.model();
  model._knex = this.query().clone();
  this.resetQuery();
  if (this.relatedData) model.relatedData = this.relatedData;
  return model.fetch(options);
}),

/**
...
```

#### <a name="apidoc.element.bookshelf.sync"></a>[function <span class="apidocSignatureSpan">bookshelf.</span>sync (syncing, options)](#apidoc.element.bookshelf.sync)
- description and source-code
```javascript
function Sync(syncing, options) {
  options = options || {};
  this.query = syncing.query();
  this.syncing = syncing.resetQuery();
  this.options = options;
  if (options.debug) this.query.debug();
  if (options.transacting) this.query.transacting(options.transacting);
}
```
- example usage
```shell
...
   * @param {Object=} options
   * @param {bool} [options.require=false] Trigger a {@link Collection.EmptyError} if no records are found.
   * @param {string|string[]} [options.withRelated=[]] A relation, or list of relations, to be eager loaded as part of the 'fetch
' operation.
   * @returns {Promise<Collection>}
   */
  fetch: _promise2.default.method(function (options) {
options = options ? (0, _lodash.clone)(options) : {};
return this.sync(options).select().bind(this).tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.EmptyError('EmptyResponse');
  }
})

// Now, load all of the data onto the collection as necessary.
.tap(this._handleResponse)
...
```



# <a name="apidoc.module.bookshelf.collection"></a>[module bookshelf.collection](#apidoc.module.bookshelf.collection)

#### <a name="apidoc.element.bookshelf.collection.default"></a>[function <span class="apidocSignatureSpan">bookshelf.collection.</span>default ()](#apidoc.element.bookshelf.collection.default)
- description and source-code
```javascript
default = function () {
  return Parent.apply(this, arguments);
}
```
- example usage
```shell
...
 *
 *  @returns {Promise<Collection>} A promise resolving to this {@link
 *  Collection collection}
 */
load: _promise2.default.method(function (relations, options) {
  if (!(0, _lodash.isArray)(relations)) relations = [relations];
  options = (0, _lodash.extend)({}, options, { shallow: true, withRelated: relations });
  return new _eager2.default(this.models, this.toJSON(options), new this.model()).fetch(options).return(this);
}),

/**
 * @method Collection#create
 * @description
 *
 * Convenience method to create a new {@link Model model} instance within a
...
```



# <a name="apidoc.module.bookshelf.eager"></a>[module bookshelf.eager](#apidoc.module.bookshelf.eager)

#### <a name="apidoc.element.bookshelf.eager.default"></a>[function <span class="apidocSignatureSpan">bookshelf.eager.</span>default ()](#apidoc.element.bookshelf.eager.default)
- description and source-code
```javascript
function EagerRelation() {
  (0, _classCallCheck3.default)(this, EagerRelation);
  return (0, _possibleConstructorReturn3.default)(this, (EagerRelation.__proto__ || Object.getPrototypeOf(EagerRelation)).apply(
this, arguments));
}
```
- example usage
```shell
...
 *
 *  @returns {Promise<Collection>} A promise resolving to this {@link
 *  Collection collection}
 */
load: _promise2.default.method(function (relations, options) {
  if (!(0, _lodash.isArray)(relations)) relations = [relations];
  options = (0, _lodash.extend)({}, options, { shallow: true, withRelated: relations });
  return new _eager2.default(this.models, this.toJSON(options), new this.model()).fetch(options).return(this);
}),

/**
 * @method Collection#create
 * @description
 *
 * Convenience method to create a new {@link Model model} instance within a
...
```



# <a name="apidoc.module.bookshelf.errors"></a>[module bookshelf.errors](#apidoc.module.bookshelf.errors)

#### <a name="apidoc.element.bookshelf.errors.EmptyError"></a>[function <span class="apidocSignatureSpan">bookshelf.errors.</span>EmptyError (message, obj)](#apidoc.element.bookshelf.errors.EmptyError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...
   * @param {string|string[]} [options.withRelated=[]] A relation, or list of relations, to be eager loaded as part of the 'fetch
' operation.
   * @returns {Promise<Collection>}
   */
  fetch: _promise2.default.method(function (options) {
options = options ? (0, _lodash.clone)(options) : {};
return this.sync(options).select().bind(this).tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.EmptyError('EmptyResponse');
  }
})

// Now, load all of the data onto the collection as necessary.
.tap(this._handleResponse)

// If the "withRelated" is specified, we also need to eager load all of the
...
```

#### <a name="apidoc.element.bookshelf.errors.NoRowsDeletedError"></a>[function <span class="apidocSignatureSpan">bookshelf.errors.</span>NoRowsDeletedError (message, obj)](#apidoc.element.bookshelf.errors.NoRowsDeletedError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...
 * @returns {Promise}
 */
return this.triggerThen('destroying', this, options);
    }).then(function () {
return sync.del();
    }).then(function (resp) {
if (options.require && resp === 0) {
  throw new this.constructor.NoRowsDeletedError('No Rows Deleted');
}
this.clear();

/**
 * Destroyed event.
 *
 * Fired before a 'delete' query. A promise may be returned from the event
...
```

#### <a name="apidoc.element.bookshelf.errors.NoRowsUpdatedError"></a>[function <span class="apidocSignatureSpan">bookshelf.errors.</span>NoRowsUpdatedError (message, obj)](#apidoc.element.bookshelf.errors.NoRowsUpdatedError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...
if (method === 'insert' && this.id == null) {
  var updatedCols = {};
  updatedCols[this.idAttribute] = this.id = resp[0];
  var updatedAttrs = this.parse(updatedCols);
  _lodash2.default.assign(this.attributes, updatedAttrs);
} else if (method === 'update' && resp === 0) {
  if (options.require !== false) {
    throw new this.constructor.NoRowsUpdatedError('No Rows Updated');
  }
}

// In case we need to reference the 'previousAttributes' for the this
// in the following event handlers.
options.previousAttributes = this._previousAttributes;
...
```

#### <a name="apidoc.element.bookshelf.errors.NotFoundError"></a>[function <span class="apidocSignatureSpan">bookshelf.errors.</span>NotFoundError (message, obj)](#apidoc.element.bookshelf.errors.NotFoundError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...

// Run the 'first' call on the 'sync' object to fetch a single model.
return this.sync(options).first(attributes).bind(this)

// Jump the rest of the chain if the response doesn't exist...
.tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.NotFoundError('EmptyResponse');
  }
})

// Now, load all of the data into the model as necessary.
.tap(this._handleResponse)

// If the "withRelated" is specified, we also need to eager load all of the
...
```



# <a name="apidoc.module.bookshelf.helpers"></a>[module bookshelf.helpers](#apidoc.module.bookshelf.helpers)

#### <a name="apidoc.element.bookshelf.helpers.deprecate"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>deprecate (a, b)](#apidoc.element.bookshelf.helpers.deprecate)
- description and source-code
```javascript
function deprecate(a, b) {
  helpers.warn(a + ' has been deprecated, please use ' + b + ' instead');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bookshelf.helpers.error"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>error (msg)](#apidoc.element.bookshelf.helpers.error)
- description and source-code
```javascript
function error(msg) {
  console.log(chalk.red(msg));
}
```
- example usage
```shell
...
var Tag = bookshelf.Model.extend({
  tableName: 'tags'
})

User.where('id', 1).fetch({withRelated: ['posts.tags']}).then(function(user) {
  console.log(user.related('posts').toJSON());
}).catch(function(err) {
  console.error(err);
});
'''

## Plugins

* [Registry](https://github.com/tgriesser/bookshelf/wiki/Plugin:-Model-Registry): Register models in a central location so that
you can refer to them using a string in relations instead of having to require it every time. Helps deal with the challenges of
circular module dependencies in Node.
* [Virtuals](https://github.com/tgriesser/bookshelf/wiki/Plugin:-Virtuals): Define virtual properties on your model to compute new
 values.
...
```

#### <a name="apidoc.element.bookshelf.helpers.morphCandidate"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>morphCandidate (candidates, foreignTable)](#apidoc.element.bookshelf.helpers.morphCandidate)
- description and source-code
```javascript
function morphCandidate(candidates, foreignTable) {
  var Target = _.find(candidates, function (Candidate) {
    return _.result(Candidate.prototype, 'tableName') === foreignTable;
  });
  if (!Target) {
    throw new Error('The target polymorphic model was not found');
  }
  return Target;
}
```
- example usage
```shell
...
    _columnNames$2 = _columnNames[1],
    idColumn = _columnNames$2 === undefined ? morphName + '_id' : _columnNames$2;

var parentsByType = _lodash2.default.groupBy(this.parent, function (model) {
  return model.get(typeColumn);
});
var TargetByType = _lodash2.default.mapValues(parentsByType, function (parents, type) {
  return _helpers2.default.morphCandidate(relatedData.candidates, type);
});

return _promise2.default.all(_lodash2.default.map(parentsByType, function (parents, type) {
  var Target = TargetByType[type];
  var idAttribute = _lodash2.default.result(Target.prototype, 'idAttribute');
  var ids = getAttributeUnique(parents, idColumn);
...
```

#### <a name="apidoc.element.bookshelf.helpers.orderBy"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>orderBy (obj, sort, order)](#apidoc.element.bookshelf.helpers.orderBy)
- description and source-code
```javascript
function orderBy(obj, sort, order) {

  var tableName = void 0;
  var idAttribute = void 0;

  if (obj.model) {
    tableName = obj.model.prototype.tableName;
    idAttribute = obj.model.prototype.idAttribute ? obj.model.prototype.idAttribute : 'id';
  } else {
    tableName = obj.constructor.prototype.tableName;
    idAttribute = obj.constructor.prototype.idAttribute ? obj.constructor.prototype.idAttribute : 'id';
  }

  var _sort = void 0;

  if (sort && sort.indexOf('-') === 0) {
    _sort = sort.slice(1);
  } else if (sort) {
    _sort = sort;
  } else {
    _sort = idAttribute;
  }

  var _order = order || (sort && sort.indexOf('-') === 0 ? 'DESC' : 'ASC');

  if (_sort.indexOf('.') === -1) {
    _sort = tableName + '.' + _sort;
  }

  return obj.query(function (qb) {
    qb.orderBy(_sort, _order);
  });
}
```
- example usage
```shell
...
* name. 'orderBy("date", 'DESC')' is the same as 'orderBy("-date")'.
*
* Unless specified using dot notation (i.e., "table.column"), the default
* table will be the table name of the model 'orderBy' was called on.
*
* @example
*
* Cars.forge().orderBy('color', 'ASC').fetch()
*    .then(function (rows) { // ...
*
* @param sort {string}
*   Column to sort on
* @param order {string}
*   Ascending ('ASC') or descending ('DESC') order
*/
...
```

#### <a name="apidoc.element.bookshelf.helpers.query"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>query (obj, args)](#apidoc.element.bookshelf.helpers.query)
- description and source-code
```javascript
function query(obj, args) {

  // Ensure the object has a query builder.
  if (!obj._knex) {
    var tableName = _.result(obj, 'tableName');
    obj._knex = obj._builder(tableName);
  }

  // If there are no arguments, return the query builder.
  if (args.length === 0) return obj._knex;

  var method = args[0];

  if (_.isFunction(method)) {

    // 'method' is a query builder callback. Call it on the query builder
    // object.
    method.call(obj._knex, obj._knex);
  } else if (_.isObject(method)) {

    // 'method' is an object. Use keys as methods and values as arguments to
    // the query builder.
    for (var key in method) {
      var target = _.isArray(method[key]) ? method[key] : [method[key]];
      obj._knex[key].apply(obj._knex, target);
    }
  } else {

    // Otherwise assume that the 'method' is string name of a query builder
    // method, and use the remaining args as arguments to that method.
    obj._knex[method].apply(obj._knex, args.slice(1));
  }
  return obj;
}
```
- example usage
```shell
...
* Get the number of records in the collection's table.
*
* @example
*
* // select count(*) from shareholders where company_id = 1 and share &gt; 0.1;
* Company.forge({id:1})
*   .shareholders()
*   .query('where', 'share', '>', '0.1')
*   .count()
*   .then(function(count) {
*     assert(count === 3);
*   });
*
* @param {string} [column='*']
*   Specify a column to count - rows with null values in this column will be excluded.
...
```

#### <a name="apidoc.element.bookshelf.helpers.saveConstraints"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>saveConstraints (model, relatedData)](#apidoc.element.bookshelf.helpers.saveConstraints)
- description and source-code
```javascript
function saveConstraints(model, relatedData) {
  var data = {};
  if (relatedData && !relatedData.isThrough() && relatedData.type !== 'belongsToMany' && relatedData.type !== 'belongsTo') {
    data[relatedData.key('foreignKey')] = relatedData.parentFk || model.get(relatedData.key('foreignKey'));
    if (relatedData.isMorph()) data[relatedData.key('morphKey')] = relatedData.key('morphValue');
  }
  return model.set(model.parse(data));
}
```
- example usage
```shell
...

  // If we've already added things on the query chain,
  // these are likely intended for the model.
  if (this._knex) {
    model._knex = this._knex;
    this.resetQuery();
  }
  return _helpers2.default.saveConstraints(model, relatedData).save(null, options).bind(this).then(function () {
    if (relatedData && relatedData.type === 'belongsToMany') {
      return this.attach(model, (0, _lodash.omit)(options, 'query'));
    }
  }).then(function () {
    this.add(model, options);
  }).return(model);
}),
...
```

#### <a name="apidoc.element.bookshelf.helpers.warn"></a>[function <span class="apidocSignatureSpan">bookshelf.helpers.</span>warn (msg)](#apidoc.element.bookshelf.helpers.warn)
- description and source-code
```javascript
function warn(msg) {
  console.log(chalk.yellow(msg));
}
```
- example usage
```shell
...
  },

  warn: function warn(msg) {
console.log(chalk.yellow(msg));
  },

  deprecate: function deprecate(a, b) {
helpers.warn(a + ' has been deprecated, please use ' + b + ' instead');
  },

  orderBy: function orderBy(obj, sort, order) {

var tableName = void 0;
var idAttribute = void 0;
...
```



# <a name="apidoc.module.bookshelf.model"></a>[module bookshelf.model](#apidoc.module.bookshelf.model)

#### <a name="apidoc.element.bookshelf.model.model"></a>[function <span class="apidocSignatureSpan">bookshelf.</span>model ()](#apidoc.element.bookshelf.model.model)
- description and source-code
```javascript
model = function () {
  return Parent.apply(this, arguments);
}
```
- example usage
```shell
...
 *  Optionally run the query in a transaction.
 *
 * @throws {Model.NotFoundError}
 * @returns {Promise<Model|null>}
 *  A promise resolving to the fetched {@link Model model} or 'null' if none exists.
 */
fetchOne: _promise2.default.method(function (options) {
  var model = new this.model();
  model._knex = this.query().clone();
  this.resetQuery();
  if (this.relatedData) model.relatedData = this.relatedData;
  return model.fetch(options);
}),

/**
...
```

#### <a name="apidoc.element.bookshelf.model.NoRowsDeletedError"></a>[function <span class="apidocSignatureSpan">bookshelf.model.</span>NoRowsDeletedError (message, obj)](#apidoc.element.bookshelf.model.NoRowsDeletedError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...
 * @returns {Promise}
 */
return this.triggerThen('destroying', this, options);
    }).then(function () {
return sync.del();
    }).then(function (resp) {
if (options.require && resp === 0) {
  throw new this.constructor.NoRowsDeletedError('No Rows Deleted');
}
this.clear();

/**
 * Destroyed event.
 *
 * Fired before a 'delete' query. A promise may be returned from the event
...
```

#### <a name="apidoc.element.bookshelf.model.NoRowsUpdatedError"></a>[function <span class="apidocSignatureSpan">bookshelf.model.</span>NoRowsUpdatedError (message, obj)](#apidoc.element.bookshelf.model.NoRowsUpdatedError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...
if (method === 'insert' && this.id == null) {
  var updatedCols = {};
  updatedCols[this.idAttribute] = this.id = resp[0];
  var updatedAttrs = this.parse(updatedCols);
  _lodash2.default.assign(this.attributes, updatedAttrs);
} else if (method === 'update' && resp === 0) {
  if (options.require !== false) {
    throw new this.constructor.NoRowsUpdatedError('No Rows Updated');
  }
}

// In case we need to reference the 'previousAttributes' for the this
// in the following event handlers.
options.previousAttributes = this._previousAttributes;
...
```

#### <a name="apidoc.element.bookshelf.model.NotFoundError"></a>[function <span class="apidocSignatureSpan">bookshelf.model.</span>NotFoundError (message, obj)](#apidoc.element.bookshelf.model.NotFoundError)
- description and source-code
```javascript
function ErrorCtor(message, obj) {
  attachProps(this, properties);
  attachProps(this, obj);
  this.message = (message || this.message);
  if (message instanceof Error) {
    this.message = message.message;
    this.stack = message.stack;
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, this.constructor);
  }
}
```
- example usage
```shell
...

// Run the 'first' call on the 'sync' object to fetch a single model.
return this.sync(options).first(attributes).bind(this)

// Jump the rest of the chain if the response doesn't exist...
.tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.NotFoundError('EmptyResponse');
  }
})

// Now, load all of the data into the model as necessary.
.tap(this._handleResponse)

// If the "withRelated" is specified, we also need to eager load all of the
...
```

#### <a name="apidoc.element.bookshelf.model.extend"></a>[function <span class="apidocSignatureSpan">bookshelf.model.</span>extend (protoProps, staticProps)](#apidoc.element.bookshelf.model.extend)
- description and source-code
```javascript
function extend(protoProps, staticProps) {
  var Parent = this;

  // The constructor function for the new subclass is either defined by you
  // (the "constructor" property in your 'extend' definition), or defaulted
  // by us to simply call the parent's constructor.
  var Child = protoProps && protoProps.hasOwnProperty('constructor') ? protoProps.constructor : function () {
    return Parent.apply(this, arguments);
  };

  (0, _lodash.assign)(Child, Parent, staticProps);

  // Set the prototype chain to inherit from 'Parent'.
  Child.prototype = Object.create(Parent.prototype, {
    constructor: {
      value: Child,
      enumerable: false,
      writable: true,
      configurable: true
    }
  });

  if (protoProps) {
    (0, _lodash.assign)(Child.prototype, protoProps);
  }

  // Give child access to the parent prototype as part of "super"
  Child.__super__ = Parent.prototype;

  // If there is an "extended" function set on the parent,
  // call it with the extended child object.
  if ((0, _lodash.isFunction)(Parent.extended)) Parent.extended(Child);

  return Child;
}
```
- example usage
```shell
...
    database : 'myapp_test',
    charset  : 'utf8'
  }
});

var bookshelf = require('bookshelf')(knex);

var User = bookshelf.Model.extend({
  tableName: 'users'
});
'''

This initialization should likely only ever happen once in your application. As it creates a connection pool for the current database
, you should use the 'bookshelf' instance returned throughout your library. You'll need to store this instance created by the initialize
 somewhere in the application so you can reference it. A common pattern to follow is to initialize the client in a module so you
 can easily reference it later:

'''js
...
```

#### <a name="apidoc.element.bookshelf.model.extended"></a>[function <span class="apidocSignatureSpan">bookshelf.model.</span>extended (child)](#apidoc.element.bookshelf.model.extended)
- description and source-code
```javascript
function extended(child) {
<span class="apidocCodeCommentSpan">  /**
   * @class Model.NotFoundError
   * @description
   *
   *   Thrown when no records are found by {@link Model#fetch fetch} or
   *   {@link Model#refresh} when called with the
   *   '{require: true}' option.
   */
</span>  child.NotFoundError = (0, _createError2.default)(this.NotFoundError);

  /**
   * @class Model.NoRowsUpdatedError
   * @description
   *
   *   Thrown when no records are saved by {@link Model#save save}
   *   unless called with the '{require: false}' option.
   */
  child.NoRowsUpdatedError = (0, _createError2.default)(this.NoRowsUpdatedError);

  /**
   * @class Model.NoRowsDeletedError
   * @description
   *
   *   Thrown when no record is deleted by {@link Model#destroy destroy}
   *   if called with the '{require: true}' option.
   */
  child.NoRowsDeletedError = (0, _createError2.default)(this.NoRowsDeletedError);
}
```
- example usage
```shell
...
  }

  // Give child access to the parent prototype as part of "super"
  Child.__super__ = Parent.prototype;

  // If there is an "extended" function set on the parent,
  // call it with the extended child object.
  if ((0, _lodash.isFunction)(Parent.extended)) Parent.extended(Child);

  return Child;
};
...
```

#### <a name="apidoc.element.bookshelf.model.super_"></a>[function <span class="apidocSignatureSpan">bookshelf.model.</span>super_ ()](#apidoc.element.bookshelf.model.super_)
- description and source-code
```javascript
function Events() {
  (0, _classCallCheck3.default)(this, Events);
  return (0, _possibleConstructorReturn3.default)(this, (Events.__proto__ || Object.getPrototypeOf(Events)).apply(this, arguments
));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bookshelf.model.prototype"></a>[module bookshelf.model.prototype](#apidoc.module.bookshelf.model.prototype)

#### <a name="apidoc.element.bookshelf.model.prototype._doFetch"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_doFetch ()](#apidoc.element.bookshelf.model.prototype._doFetch)
- description and source-code
```javascript
_doFetch = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
 */
refresh: function refresh(options) {

  // If this is new, we use all its attributes. Otherwise we just grab the
  // primary key.
  var attributes = this.isNew() ? this.attributes : _lodash2.default.pick(this.attributes, this.idAttribute);

  return this._doFetch(attributes, options);
},


/**
 * Fetches a {@link Model model} from the database, using any {@link
 * Model#attributes attributes} currently set on the model to form a 'select'
 * query.
...
```

#### <a name="apidoc.element.bookshelf.model.prototype._handleEager"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_handleEager (response, options)](#apidoc.element.bookshelf.model.prototype._handleEager)
- description and source-code
```javascript
function _handleEager(response, options) {
  return new _eager2.default([this], response, this).fetch(options);
}
```
- example usage
```shell
...

    // If the "withRelated" is specified, we also need to eager load all of the
    // data on the collection, as a side-effect, before we ultimately jump into the
    // next step of the collection. Since the 'columns' are only relevant to the current
    // level, ensure those are omitted from the options.
    .tap(function (response) {
if (options.withRelated) {
  return this._handleEager(response, (0, _lodash.omit)(options, 'columns'));
}
    }).tap(function (response) {

/**
 * @event Collection#fetched
 *
 * @description
...
```

#### <a name="apidoc.element.bookshelf.model.prototype._handleResponse"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_handleResponse (response)](#apidoc.element.bookshelf.model.prototype._handleResponse)
- description and source-code
```javascript
function _handleResponse(response) {
  var relatedData = this.relatedData;
  this.set(this.parse(response[0]), { silent: true })._reset();
  if (relatedData && relatedData.isJoined()) {
    relatedData.parsePivot([this]);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bookshelf.model.prototype._morphOneOrMany"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>_morphOneOrMany (Target, morphName, columnNames, morphValue, type)](#apidoc.element.bookshelf.model.prototype._morphOneOrMany)
- description and source-code
```javascript
function _morphOneOrMany(Target, morphName, columnNames, morphValue, type) {
  if (!_lodash2.default.isArray(columnNames)) {
    // Shift by one place
    morphValue = columnNames;
    columnNames = null;
  }
  if (!morphName || !Target) throw new Error('The polymorphic 'name' and 'Target' are required.');
  return this._relation(type, Target, { morphName: morphName, morphValue: morphValue, columnNames: columnNames }).init(this);
}
```
- example usage
```shell
...
 *   The string value associated with this relationship. Stored in the '_type'
 *   column of the polymorphic table. Defaults to 'Target#{@link
 *   Model#tableName tableName}'.
 *
 * @returns {Model} The related model.
 */
morphOne: function morphOne(Target, name, columnNames, morphValue) {
  return this._morphOneOrMany(Target, name, columnNames, morphValue, 'morphOne');
},


/**
 * {@link Model#morphMany morphMany} is essentially the same as a {@link
 * Model#morphOne morphOne}, but creating a {@link Collection collection}
 * rather than a {@link Model model} (similar to a {@link Model#hasOne
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.all"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>all ()](#apidoc.element.bookshelf.model.prototype.all)
- description and source-code
```javascript
function all() {
  var collection = this.constructor.collection();
  collection._knex = this.query().clone();
  this.resetQuery();
  if (this.relatedData) collection.relatedData = this.relatedData;
  return collection;
}
```
- example usage
```shell
...
      var parentsByType = _lodash2.default.groupBy(this.parent, function (model) {
return model.get(typeColumn);
      });
      var TargetByType = _lodash2.default.mapValues(parentsByType, function (parents, type) {
return _helpers2.default.morphCandidate(relatedData.candidates, type);
      });

      return _promise2.default.all(_lodash2.default.map(parentsByType, function (parents, type) {
var Target = TargetByType[type];
var idAttribute = _lodash2.default.result(Target.prototype, 'idAttribute');
var ids = getAttributeUnique(parents, idColumn);

return Target.query('whereIn', idAttribute, ids).sync(options).select().tap(function (response) {
  var clone = relatedData.instance('morphTo', Target, { morphName: morphName, columnNames: columnNames });
  return _this3._eagerLoadHelper(response, relationName, { relatedData: clone }, options);
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.belongsTo"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>belongsTo (Target, foreignKey, foreignKeyTarget)](#apidoc.element.bookshelf.model.prototype.belongsTo)
- description and source-code
```javascript
function belongsTo(Target, foreignKey, foreignKeyTarget) {
  return this._relation('belongsTo', Target, { foreignKey: foreignKey, foreignKeyTarget: foreignKeyTarget }).init(this);
}
```
- example usage
```shell
...
* Model#belongsTo belongsTo} relationship is used for a model that is a
* member of another Target model, referenced by the foreignKey in the current
* model.
*
*     let Book = bookshelf.Model.extend({
*       tableName: 'books',
*       author: function() {
*         return this.belongsTo(Author);
*       }
*     });
*
*     // select * from 'books' where id = 1
*     // select * from 'authors' where id = book.author_id
*     Book.where({id: 1}).fetch({withRelated: ['author']}).then(function(book) {
*       console.log(JSON.stringify(book.related('author')));
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.belongsToMany"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>belongsToMany (Target, joinTableName, foreignKey, otherKey, foreignKeyTarget, otherKeyTarget)](#apidoc.element.bookshelf.model.prototype.belongsToMany)
- description and source-code
```javascript
function belongsToMany(Target, joinTableName, foreignKey, otherKey, foreignKeyTarget, otherKeyTarget) {
  return this._relation('belongsToMany', Target, {
    joinTableName: joinTableName, foreignKey: foreignKey, otherKey: otherKey, foreignKeyTarget: foreignKeyTarget, otherKeyTarget
: otherKeyTarget
  }).init(this);
}
```
- example usage
```shell
...
    return this.hasMany(Posts);
  }
});

var Posts = bookshelf.Model.extend({
  tableName: 'messages',
  tags: function() {
    return this.belongsToMany(Tag);
  }
});

var Tag = bookshelf.Model.extend({
  tableName: 'tags'
})
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.clone"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>clone ()](#apidoc.element.bookshelf.model.prototype.clone)
- description and source-code
```javascript
function clone() {
  // This needs to use the direct apply method because the spread operator
  // incorrectly converts to 'clone.apply(ModelBase.prototype, arguments)'
  // instead of 'apply(this, arguments)'
  var cloned = BookshelfModel.__super__.clone.apply(this, arguments);
  if (this._knex != null) {
    cloned._knex = cloned._builder(this._knex.clone());
  }
  return cloned;
}
```
- example usage
```shell
...
 *
 * @throws {Model.NotFoundError}
 * @returns {Promise<Model|null>}
 *  A promise resolving to the fetched {@link Model model} or 'null' if none exists.
 */
fetchOne: _promise2.default.method(function (options) {
  var model = new this.model();
  model._knex = this.query().clone();
  this.resetQuery();
  if (this.relatedData) model.relatedData = this.relatedData;
  return model.fetch(options);
}),

/**
 * @method Collection#load
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.count"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>count (column, options)](#apidoc.element.bookshelf.model.prototype.count)
- description and source-code
```javascript
function count(column, options) {
  return this.all().count(column, options);
}
```
- example usage
```shell
...
*
* @example
*
* // select count(*) from shareholders where company_id = 1 and share &gt; 0.1;
* Company.forge({id:1})
*   .shareholders()
*   .query('where', 'share', '>', '0.1')
*   .count()
*   .then(function(count) {
*     assert(count === 3);
*   });
*
* @param {string} [column='*']
*   Specify a column to count - rows with null values in this column will be excluded.
* @param {Object=} options
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.destroy"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>destroy ()](#apidoc.element.bookshelf.model.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...

Make sure you check that the type is correct for the initial parameters passed to the initial model being fetched. For example '
new Model({id: '1'}).load([relations...])' will not return the same as 'Model({id: 1}).load([relations...])' - notice that the id
 is a string in one case and a number in the other. This can be a common mistake if retrieving the id from a url parameter.

This is only an issue if you're eager loading data with load without first fetching the original model. 'Model({id: '1'}).fetch({
withRelated: [relations...]})' should work just fine.

### My process won't exit after my script is finished, why?

The issue here is that Knex, the database abstraction layer used by Bookshelf, uses connection pooling and thus keeps the database
 connection open. If you want your process to exit after your script has finished, you will have to call '.destroy(cb)' on the '
knex' property of your 'Bookshelf' instance or on the 'Knex' instance passed during initialization. More information about connection
 pooling can be found over at the [Knex docs](http://knexjs.org/#Installation-pooling).

### How do I debug?

If you pass '{debug: true}' as one of the options in your initialize settings, you can see all of the query calls being made. Sometimes
 you need to dive a bit further into the various calls and see what all is going on behind the scenes. I'd recommend [node-inspector
](https://github.com/dannycoates/node-inspector), which allows you to debug code with 'debugger' statements like you would in the
 browser.

Bookshelf uses its own copy of the "bluebird" promise library, you can read up here for more on debugging these promises... but
in short, adding:
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.fetch"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>fetch (options)](#apidoc.element.bookshelf.model.prototype.fetch)
- description and source-code
```javascript
function fetch(options) {

  // Fetch uses all set attributes.
  return this._doFetch(this.attributes, options);
}
```
- example usage
```shell
...
  }
});

var Tag = bookshelf.Model.extend({
  tableName: 'tags'
})

User.where('id', 1).fetch({withRelated: ['posts.tags']}).then(function(user) {
  console.log(user.related('posts').toJSON());
}).catch(function(err) {
  console.error(err);
});
'''

## Plugins
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.fetchAll"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>fetchAll (options)](#apidoc.element.bookshelf.model.prototype.fetchAll)
- description and source-code
```javascript
function fetchAll(options) {
  var _this = this;

  var collection = this.all();
  return collection.once('fetching', function (__, columns, opts) {
<span class="apidocCodeCommentSpan">    /**
     * Fired before a {@link Model#fetchAll fetchAll} operation. A promise
     * may be returned from the event handler for async behaviour.
     *
     * @event Model#"fetching:collection"
     * @param {Model}    collection The collection that has been fetched.
     * @param {string[]} columns    The columns being retrieved by the query.
     * @param {Object}   options    Options object passed to {@link Model#fetchAll fetchAll}.
     * @returns {Promise}
     */
</span>    return _this.triggerThen('fetching:collection', collection, columns, opts);
  }).once('fetched', function (__, resp, opts) {
    /**
     * Fired after a {@link Model#fetchAll fetchAll} operation. A promise
     * may be returned from the event handler for async behaviour.
     *
     * @event Model#"fetched:collection"
     * @param {Model}  collection The collection that has been fetched.
     * @param {Object} resp       The Knex query response.
     * @param {Object} options    Options object passed to {@link Model#fetchAll fetchAll}.
     * @returns {Promise}
     */
    return _this.triggerThen('fetched:collection', collection, resp, opts);
  }).fetch(options);
}
```
- example usage
```shell
...
* name. 'orderBy("date", 'DESC')' is the same as 'orderBy("-date")'.
*
* Unless specified using dot notation (i.e., "table.column"), the default
* table will be the table name of the model 'orderBy' was called on.
*
* @example
*
* Car.forge().orderBy('color', 'ASC').fetchAll()
*    .then(function (rows) { // ...
*
* @param sort {string}
*   Column to sort on
* @param order {string}
*   Ascending ('ASC') or descending ('DESC') order
*/
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.hasMany"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>hasMany (Target, foreignKey, foreignKeyTarget)](#apidoc.element.bookshelf.model.prototype.hasMany)
- description and source-code
```javascript
function hasMany(Target, foreignKey, foreignKeyTarget) {
  return this._relation('hasMany', Target, { foreignKey: foreignKey, foreignKeyTarget: foreignKeyTarget }).init(this);
}
```
- example usage
```shell
...
'''js
var knex = require('knex')({client: 'mysql', connection: process.env.MYSQL_DATABASE_CONNECTION });
var bookshelf = require('bookshelf')(knex);

var User = bookshelf.Model.extend({
tableName: 'users',
posts: function() {
  return this.hasMany(Posts);
}
});

var Posts = bookshelf.Model.extend({
tableName: 'messages',
tags: function() {
  return this.belongsToMany(Tag);
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.hasOne"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>hasOne (Target, foreignKey, foreignKeyTarget)](#apidoc.element.bookshelf.model.prototype.hasOne)
- description and source-code
```javascript
function hasOne(Target, foreignKey, foreignKeyTarget) {
  return this._relation('hasOne', Target, { foreignKey: foreignKey, foreignKeyTarget: foreignKeyTarget }).init(this);
}
```
- example usage
```shell
...
*     let Record = bookshelf.Model.extend({
*       tableName: 'health_records'
*     });
*
*     let Patient = bookshelf.Model.extend({
*       tableName: 'patients',
*       record: function() {
*         return this.hasOne(Record);
*       }
*     });
*
*     // select * from 'health_records' where 'patient_id' = 1;
*     new Patient({id: 1}).related('record').fetch().then(function(model) {
*       // ...
*     });
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.load"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>load ()](#apidoc.element.bookshelf.model.prototype.load)
- description and source-code
```javascript
load = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...

### Can I use standard node.js style callbacks?

Yes - you can call '.asCallback(function(err, resp) {' on any "sync" method and use the standard '(err, result)' style callback
interface if you prefer.

### My relations don't seem to be loading, what's up?

Make sure you check that the type is correct for the initial parameters passed to the initial model being fetched. For example '
new Model({id: '1'}).load([relations...])' will not return the same as 'Model({id: 1}).load([relations...])' - notice that the id
 is a string in one case and a number in the other. This can be a common mistake if retrieving the id from a url parameter.

This is only an issue if you're eager loading data with load without first fetching the original model. 'Model({id: '1'}).fetch({
withRelated: [relations...]})' should work just fine.

### My process won't exit after my script is finished, why?

The issue here is that Knex, the database abstraction layer used by Bookshelf, uses connection pooling and thus keeps the database
 connection open. If you want your process to exit after your script has finished, you will have to call '.destroy(cb)' on the '
knex' property of your 'Bookshelf' instance or on the 'Knex' instance passed during initialization. More information about connection
 pooling can be found over at the [Knex docs](http://knexjs.org/#Installation-pooling).
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.morphMany"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>morphMany (Target, name, columnNames, morphValue)](#apidoc.element.bookshelf.model.prototype.morphMany)
- description and source-code
```javascript
function morphMany(Target, name, columnNames, morphValue) {
  return this._morphOneOrMany(Target, name, columnNames, morphValue, 'morphMany');
}
```
- example usage
```shell
...
* and 'imageable_id'. The 'morphValue' may be optionally set to
* store/retrieve a different value in the '_type' column than the 'Target''s
* {@link Model#tableName tableName}.
*
*     let Post = bookshelf.Model.extend({
*       tableName: 'posts',
*       photos: function() {
*         return this.morphMany(Photo, 'imageable');
*       }
*     });
*
* And with custom columnNames:
*
*     let Post = bookshelf.Model.extend({
*       tableName: 'posts',
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.morphOne"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>morphOne (Target, name, columnNames, morphValue)](#apidoc.element.bookshelf.model.prototype.morphOne)
- description and source-code
```javascript
function morphOne(Target, name, columnNames, morphValue) {
  return this._morphOneOrMany(Target, name, columnNames, morphValue, 'morphOne');
}
```
- example usage
```shell
...
* below the table names would be 'imageable_type' and 'imageable_id'. The
* 'morphValue' may be optionally set to store/retrieve a different value in
* the '_type' column than the {@link Model#tableName}.
*
*     let Site = bookshelf.Model.extend({
*       tableName: 'sites',
*       photo: function() {
*         return this.morphOne(Photo, 'imageable');
*       }
*     });
*
* And with custom 'columnNames':
*
*     let Site = bookshelf.Model.extend({
*       tableName: 'sites',
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.morphTo"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>morphTo (morphName)](#apidoc.element.bookshelf.model.prototype.morphTo)
- description and source-code
```javascript
function morphTo(morphName) {
  if (!_lodash2.default.isString(morphName)) throw new Error('The 'morphTo' name must be specified.');
  var columnNames = void 0,
      candidates = void 0;
  if (_lodash2.default.isArray(arguments[1])) {
    columnNames = arguments[1];
    candidates = _lodash2.default.drop(arguments, 2);
  } else {
    columnNames = null;
    candidates = _lodash2.default.drop(arguments);
  }
  return this._relation('morphTo', null, { morphName: morphName, columnNames: columnNames, candidates: candidates }).init(this);
}
```
- example usage
```shell
...
* morphMany} relations, where the 'targets' must be passed to signify which
* {@link Model models} are the potential opposite end of the {@link
* polymorphicRelation polymorphic relation}.
*
*     let Photo = bookshelf.Model.extend({
*       tableName: 'photos',
*       imageable: function() {
*         return this.morphTo('imageable', Site, Post);
*       }
*     });
*
* And with custom columnNames:
*
*     let Photo = bookshelf.Model.extend({
*       tableName: 'photos',
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.orderBy"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>orderBy ()](#apidoc.element.bookshelf.model.prototype.orderBy)
- description and source-code
```javascript
function orderBy() {
  for (var _len2 = arguments.length, args = Array(_len2), _key2 = 0; _key2 < _len2; _key2++) {
    args[_key2] = arguments[_key2];
  }

  return _helpers2.default.orderBy.apply(_helpers2.default, [this].concat(args));
}
```
- example usage
```shell
...
* name. 'orderBy("date", 'DESC')' is the same as 'orderBy("-date")'.
*
* Unless specified using dot notation (i.e., "table.column"), the default
* table will be the table name of the model 'orderBy' was called on.
*
* @example
*
* Cars.forge().orderBy('color', 'ASC').fetch()
*    .then(function (rows) { // ...
*
* @param sort {string}
*   Column to sort on
* @param order {string}
*   Ascending ('ASC') or descending ('DESC') order
*/
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.query"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>query ()](#apidoc.element.bookshelf.model.prototype.query)
- description and source-code
```javascript
function query() {
  return _helpers2.default.query(this, _lodash2.default.toArray(arguments));
}
```
- example usage
```shell
...
* Get the number of records in the collection's table.
*
* @example
*
* // select count(*) from shareholders where company_id = 1 and share &gt; 0.1;
* Company.forge({id:1})
*   .shareholders()
*   .query('where', 'share', '>', '0.1')
*   .count()
*   .then(function(count) {
*     assert(count === 3);
*   });
*
* @param {string} [column='*']
*   Specify a column to count - rows with null values in this column will be excluded.
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.refresh"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>refresh (options)](#apidoc.element.bookshelf.model.prototype.refresh)
- description and source-code
```javascript
function refresh(options) {

  // If this is new, we use all its attributes. Otherwise we just grab the
  // primary key.
  var attributes = this.isNew() ? this.attributes : _lodash2.default.pick(this.attributes, this.idAttribute);

  return this._doFetch(attributes, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bookshelf.model.prototype.resetQuery"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>resetQuery ()](#apidoc.element.bookshelf.model.prototype.resetQuery)
- description and source-code
```javascript
function resetQuery() {
  this._knex = null;
  return this;
}
```
- example usage
```shell
...
 * @throws {Model.NotFoundError}
 * @returns {Promise<Model|null>}
 *  A promise resolving to the fetched {@link Model model} or 'null' if none exists.
 */
fetchOne: _promise2.default.method(function (options) {
  var model = new this.model();
  model._knex = this.query().clone();
  this.resetQuery();
  if (this.relatedData) model.relatedData = this.relatedData;
  return model.fetch(options);
}),

/**
 * @method Collection#load
 * @description
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.save"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>save ()](#apidoc.element.bookshelf.model.prototype.save)
- description and source-code
```javascript
save = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
*
* When used on a relation, 'create' will automatically set foreign key
* attributes before persisting the 'Model'.
*
* '''
* const { courses, ...attributes } = req.body;
*
* Student.forge(attributes).save().tap(student =>
*   Promise.map(courses, course => student.related('courses').create(course))
* ).then(student =>
*   res.status(200).send(student)
* ).catch(error =>
*   res.status(500).send(error.message)
* );
* '''
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.sync"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>sync (options)](#apidoc.element.bookshelf.model.prototype.sync)
- description and source-code
```javascript
function sync(options) {
  return new _sync2.default(this, options);
}
```
- example usage
```shell
...
   * @param {Object=} options
   * @param {bool} [options.require=false] Trigger a {@link Collection.EmptyError} if no records are found.
   * @param {string|string[]} [options.withRelated=[]] A relation, or list of relations, to be eager loaded as part of the 'fetch
' operation.
   * @returns {Promise<Collection>}
   */
  fetch: _promise2.default.method(function (options) {
options = options ? (0, _lodash.clone)(options) : {};
return this.sync(options).select().bind(this).tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.EmptyError('EmptyResponse');
  }
})

// Now, load all of the data onto the collection as necessary.
.tap(this._handleResponse)
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.through"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>through (Interim, throughForeignKey, otherKey, throughForeignKeyTarget, otherKeyTarget)](#apidoc.element.bookshelf.model.prototype.through)
- description and source-code
```javascript
function through(Interim, throughForeignKey, otherKey, throughForeignKeyTarget, otherKeyTarget) {
  return this.relatedData.through(this, Interim, {
    throughForeignKey: throughForeignKey, otherKey: otherKey, throughForeignKeyTarget: throughForeignKeyTarget, otherKeyTarget:
otherKeyTarget
  });
}
```
- example usage
```shell
...
 *
 *   Column in this collection model which 'otherKey' references, if other
 *   than 'id' / '{@link Model#idAttribute idAttribute}'.
 *
 * @returns {Collection}
 */
through: function through(Interim, throughForeignKey, otherKey, throughForeignKeyTarget, otherKeyTarget) {
  return this.relatedData.through(this, Interim, {
    throughForeignKey: throughForeignKey, otherKey: otherKey, throughForeignKeyTarget: throughForeignKeyTarget, otherKeyTarget:
otherKeyTarget
  });
},

/**
 * @method Collection#fetch
 * @description
...
```

#### <a name="apidoc.element.bookshelf.model.prototype.where"></a>[function <span class="apidocSignatureSpan">bookshelf.model.prototype.</span>where ()](#apidoc.element.bookshelf.model.prototype.where)
- description and source-code
```javascript
function where() {
  for (var _len = arguments.length, args = Array(_len), _key = 0; _key < _len; _key++) {
    args[_key] = arguments[_key];
  }

  return this.query.apply(this, ['where'].concat(args));
}
```
- example usage
```shell
...
  }
});

var Tag = bookshelf.Model.extend({
  tableName: 'tags'
})

User.where('id', 1).fetch({withRelated: ['posts.tags']}).then(function(user) {
  console.log(user.related('posts').toJSON());
}).catch(function(err) {
  console.error(err);
});
'''

## Plugins
...
```



# <a name="apidoc.module.bookshelf.relation"></a>[module bookshelf.relation](#apidoc.module.bookshelf.relation)

#### <a name="apidoc.element.bookshelf.relation.default"></a>[function <span class="apidocSignatureSpan">bookshelf.relation.</span>default ()](#apidoc.element.bookshelf.relation.default)
- description and source-code
```javascript
default = function () {
  return Parent.apply(this, arguments);
}
```
- example usage
```shell
...
 *
 *  @returns {Promise<Collection>} A promise resolving to this {@link
 *  Collection collection}
 */
load: _promise2.default.method(function (relations, options) {
  if (!(0, _lodash.isArray)(relations)) relations = [relations];
  options = (0, _lodash.extend)({}, options, { shallow: true, withRelated: relations });
  return new _eager2.default(this.models, this.toJSON(options), new this.model()).fetch(options).return(this);
}),

/**
 * @method Collection#create
 * @description
 *
 * Convenience method to create a new {@link Model model} instance within a
...
```



# <a name="apidoc.module.bookshelf.sync"></a>[module bookshelf.sync](#apidoc.module.bookshelf.sync)

#### <a name="apidoc.element.bookshelf.sync.sync"></a>[function <span class="apidocSignatureSpan">bookshelf.</span>sync (syncing, options)](#apidoc.element.bookshelf.sync.sync)
- description and source-code
```javascript
function Sync(syncing, options) {
  options = options || {};
  this.query = syncing.query();
  this.syncing = syncing.resetQuery();
  this.options = options;
  if (options.debug) this.query.debug();
  if (options.transacting) this.query.transacting(options.transacting);
}
```
- example usage
```shell
...
   * @param {Object=} options
   * @param {bool} [options.require=false] Trigger a {@link Collection.EmptyError} if no records are found.
   * @param {string|string[]} [options.withRelated=[]] A relation, or list of relations, to be eager loaded as part of the 'fetch
' operation.
   * @returns {Promise<Collection>}
   */
  fetch: _promise2.default.method(function (options) {
options = options ? (0, _lodash.clone)(options) : {};
return this.sync(options).select().bind(this).tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.EmptyError('EmptyResponse');
  }
})

// Now, load all of the data onto the collection as necessary.
.tap(this._handleResponse)
...
```



# <a name="apidoc.module.bookshelf.sync.prototype"></a>[module bookshelf.sync.prototype](#apidoc.module.bookshelf.sync.prototype)

#### <a name="apidoc.element.bookshelf.sync.prototype.count"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>count ()](#apidoc.element.bookshelf.sync.prototype.count)
- description and source-code
```javascript
count = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
*
* @example
*
* // select count(*) from shareholders where company_id = 1 and share &gt; 0.1;
* Company.forge({id:1})
*   .shareholders()
*   .query('where', 'share', '>', '0.1')
*   .count()
*   .then(function(count) {
*     assert(count === 3);
*   });
*
* @param {string} [column='*']
*   Specify a column to count - rows with null values in this column will be excluded.
* @param {Object=} options
...
```

#### <a name="apidoc.element.bookshelf.sync.prototype.del"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>del ()](#apidoc.element.bookshelf.sync.prototype.del)
- description and source-code
```javascript
del = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
 * @event Model#destroying
 * @param {Model}  model    The model firing the event.
 * @param {Object} options  Options object passed to {@link Model#save save}.
 * @returns {Promise}
 */
return this.triggerThen('destroying', this, options);
    }).then(function () {
return sync.del();
    }).then(function (resp) {
if (options.require && resp === 0) {
  throw new this.constructor.NoRowsDeletedError('No Rows Deleted');
}
this.clear();

/**
...
```

#### <a name="apidoc.element.bookshelf.sync.prototype.first"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>first ()](#apidoc.element.bookshelf.sync.prototype.first)
- description and source-code
```javascript
first = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
  },


  _doFetch: _promise2.default.method(function (attributes, options) {
options = options ? _lodash2.default.clone(options) : {};

// Run the 'first' call on the 'sync' object to fetch a single model.
return this.sync(options).first(attributes).bind(this)

// Jump the rest of the chain if the response doesn't exist...
.tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.NotFoundError('EmptyResponse');
  }
})
...
```

#### <a name="apidoc.element.bookshelf.sync.prototype.insert"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>insert ()](#apidoc.element.bookshelf.sync.prototype.insert)
- description and source-code
```javascript
insert = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
        throw new Error('No rows were updated');
      }
      return numUpdated;
    });
  }

  return this.triggerThen('creating', this, data, options).then(function () {
    return builder.insert(data).then(function () {
      collection.add(item);
    });
  });
}),

// Loads or prepares a pivot model based on the constraints and deals with
// pivot model changes by calling the appropriate Bookshelf Model API
...
```

#### <a name="apidoc.element.bookshelf.sync.prototype.prefixFields"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>prefixFields (fields)](#apidoc.element.bookshelf.sync.prototype.prefixFields)
- description and source-code
```javascript
function prefixFields(fields) {
  var tableName = this.syncing.tableName;
  var prefixed = {};
  for (var key in fields) {
    prefixed[tableName + '.' + key] = fields[key];
  }
  return prefixed;
}
```
- example usage
```shell
...
//
// NOTE: '_.omit' returns an empty object, even if attributes are null.
var whereAttributes = _lodash2.default.omitBy(attributes, _lodash2.default.isPlainObject);

if (!_lodash2.default.isEmpty(whereAttributes)) {

  // Format and prefix attributes.
  var formatted = this.prefixFields(model.format(whereAttributes));
  query.where(formatted);
}

// Limit to a single result.
query.limit(1);

return this.select();
...
```

#### <a name="apidoc.element.bookshelf.sync.prototype.select"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>select ()](#apidoc.element.bookshelf.sync.prototype.select)
- description and source-code
```javascript
select = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
   * @param {Object=} options
   * @param {bool} [options.require=false] Trigger a {@link Collection.EmptyError} if no records are found.
   * @param {string|string[]} [options.withRelated=[]] A relation, or list of relations, to be eager loaded as part of the 'fetch
' operation.
   * @returns {Promise<Collection>}
   */
  fetch: _promise2.default.method(function (options) {
options = options ? (0, _lodash.clone)(options) : {};
return this.sync(options).select().bind(this).tap(function (response) {
  if (!response || response.length === 0) {
    throw new this.constructor.EmptyError('EmptyResponse');
  }
})

// Now, load all of the data onto the collection as necessary.
.tap(this._handleResponse)
...
```

#### <a name="apidoc.element.bookshelf.sync.prototype.update"></a>[function <span class="apidocSignatureSpan">bookshelf.sync.prototype.</span>update ()](#apidoc.element.bookshelf.sync.prototype.update)
- description and source-code
```javascript
update = function () {
    var ret = new Promise(INTERNAL);
    ret._captureStackTrace();
    ret._pushContext();
    var value = tryCatch(fn).apply(this, arguments);
    var promiseCreated = ret._popContext();
    debug.checkForgottenReturns(
        value, promiseCreated, "Promise.method", ret);
    ret._resolveFromSyncValue(value);
    return ret;
}
```
- example usage
```shell
...
    var model = collection.get(data[relatedData.key('otherKey')]);
    if (model) {
      collection.remove(model);
    }
  });
}
if (method === 'update') {
  return builder.where(data).update(item).then(function (numUpdated) {
    if (options && options.require === true && numUpdated === 0) {
      throw new Error('No rows were updated');
    }
    return numUpdated;
  });
}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
