# api documentation for  [ajv (v4.11.5)](https://github.com/epoberezkin/ajv)  [![npm package](https://img.shields.io/npm/v/npmdoc-ajv.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ajv) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ajv.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ajv)
#### Another JSON Schema Validator

[![NPM](https://nodei.co/npm/ajv.png?downloads=true)](https://www.npmjs.com/package/ajv)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ajv/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ajv_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ajv/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ajv/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ajv/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Evgeny Poberezkin"
    },
    "bugs": {
        "url": "https://github.com/epoberezkin/ajv/issues"
    },
    "dependencies": {
        "co": "^4.6.0",
        "json-stable-stringify": "^1.0.1"
    },
    "description": "Another JSON Schema Validator",
    "devDependencies": {
        "bluebird": "^3.1.5",
        "brfs": "^1.4.3",
        "browserify": "^14.1.0",
        "chai": "^3.5.0",
        "coveralls": "^2.11.4",
        "del-cli": "^0.2.1",
        "dot": "^1.0.3",
        "eslint": "^3.2.2",
        "gh-pages-generator": "^0.2.0",
        "glob": "^7.0.0",
        "if-node-version": "^1.0.0",
        "js-beautify": "^1.5.6",
        "jshint": "^2.8.0",
        "json-schema-test": "^1.1.1",
        "karma": "^1.0.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-mocha": "^1.1.1",
        "karma-phantomjs-launcher": "^1.0.0",
        "karma-sauce-launcher": "^1.1.0",
        "mocha": "^3.0.0",
        "nodent": "^3.0.2",
        "nyc": "^10.0.0",
        "phantomjs-prebuilt": "^2.1.4",
        "pre-commit": "^1.1.1",
        "regenerator": "0.9.5",
        "require-globify": "^1.3.0",
        "typescript": "^2.0.3",
        "uglify-js": "^2.6.1",
        "watch": "^1.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "b6ee74657b993a01dce44b7944d56f485828d5bd",
        "tarball": "https://registry.npmjs.org/ajv/-/ajv-4.11.5.tgz"
    },
    "files": [
        "lib/",
        "dist/",
        "scripts/",
        "LICENSE",
        ".tonic_example.js"
    ],
    "gitHead": "c0a625b1a911ef1de6a67ed8f7819cba12161ff8",
    "homepage": "https://github.com/epoberezkin/ajv",
    "keywords": [
        "JSON",
        "schema",
        "validator",
        "validation",
        "jsonschema",
        "json-schema",
        "json-schema-validator",
        "json-schema-validation"
    ],
    "license": "MIT",
    "main": "lib/ajv.js",
    "maintainers": [
        {
            "name": "blakeembrey",
            "email": "hello@blakeembrey.com"
        },
        {
            "name": "esp",
            "email": "e.poberezkin@me.com"
        }
    ],
    "name": "ajv",
    "nyc": {
        "exclude": [
            "**/spec/**",
            "node_modules"
        ],
        "reporter": [
            "lcov",
            "text-summary"
        ]
    },
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/epoberezkin/ajv.git"
    },
    "scripts": {
        "build": "del-cli lib/dotjs/*.js && node scripts/compile-dots.js",
        "bundle": "node ./scripts/bundle.js . Ajv pure_getters",
        "bundle-all": "del-cli dist && npm run bundle && npm run bundle-regenerator && npm run bundle-nodent",
        "bundle-beautify": "node ./scripts/bundle.js js-beautify",
        "bundle-nodent": "node ./scripts/bundle.js nodent",
        "bundle-regenerator": "node ./scripts/bundle.js regenerator",
        "eslint": "if-node-version \">=4\" eslint lib/*.js lib/compile/*.js spec scripts",
        "jshint": "jshint lib/*.js lib/**/*.js --exclude lib/dotjs/**/*",
        "prepublish": "npm run build && npm run bundle-all",
        "test": "npm run jshint && npm run eslint && npm run test-ts && npm run build && npm run test-cov && npm run test-browser",
        "test-browser": "del-cli .browser && npm run bundle-all && scripts/prepare-tests && npm run test-karma",
        "test-cov": "nyc npm run test-spec",
        "test-debug": "mocha spec/*.spec.js --debug-brk -R spec",
        "test-fast": "AJV_FAST_TEST=true npm run test-spec",
        "test-karma": "karma start --single-run --browsers PhantomJS",
        "test-spec": "mocha spec/*.spec.js -R spec",
        "test-ts": "tsc --target ES5 --noImplicitAny lib/ajv.d.ts",
        "watch": "watch 'npm run build' ./lib/dot"
    },
    "tonicExampleFilename": ".tonic_example.js",
    "typings": "lib/ajv.d.ts",
    "version": "4.11.5",
    "webpack": "dist/ajv.bundle.js"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ajv](#apidoc.module.ajv)
1.  [function <span class="apidocSignatureSpan">ajv.</span>ValidationError (errors)](#apidoc.element.ajv.ValidationError)
1.  [function <span class="apidocSignatureSpan">ajv.</span>cache ()](#apidoc.element.ajv.cache)
1.  object <span class="apidocSignatureSpan">ajv.</span>ValidationError.prototype
1.  object <span class="apidocSignatureSpan">ajv.</span>async
1.  object <span class="apidocSignatureSpan">ajv.</span>cache.prototype
1.  object <span class="apidocSignatureSpan">ajv.</span>keyword
1.  object <span class="apidocSignatureSpan">ajv.</span>v5

#### [module ajv.ValidationError](#apidoc.module.ajv.ValidationError)
1.  [function <span class="apidocSignatureSpan">ajv.</span>ValidationError (errors)](#apidoc.element.ajv.ValidationError.ValidationError)

#### [module ajv.ValidationError.prototype](#apidoc.module.ajv.ValidationError.prototype)
1.  [function <span class="apidocSignatureSpan">ajv.ValidationError.prototype.</span>constructor (errors)](#apidoc.element.ajv.ValidationError.prototype.constructor)

#### [module ajv.async](#apidoc.module.ajv.async)
1.  [function <span class="apidocSignatureSpan">ajv.async.</span>compile (schema, callback)](#apidoc.element.ajv.async.compile)
1.  [function <span class="apidocSignatureSpan">ajv.async.</span>setup (opts, required)](#apidoc.element.ajv.async.setup)

#### [module ajv.cache](#apidoc.module.ajv.cache)
1.  [function <span class="apidocSignatureSpan">ajv.</span>cache ()](#apidoc.element.ajv.cache.cache)

#### [module ajv.cache.prototype](#apidoc.module.ajv.cache.prototype)
1.  [function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>clear ()](#apidoc.element.ajv.cache.prototype.clear)
1.  [function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>del (key)](#apidoc.element.ajv.cache.prototype.del)
1.  [function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>get (key)](#apidoc.element.ajv.cache.prototype.get)
1.  [function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>put (key, value)](#apidoc.element.ajv.cache.prototype.put)

#### [module ajv.keyword](#apidoc.module.ajv.keyword)
1.  [function <span class="apidocSignatureSpan">ajv.keyword.</span>add (keyword, definition)](#apidoc.element.ajv.keyword.add)
1.  [function <span class="apidocSignatureSpan">ajv.keyword.</span>get (keyword)](#apidoc.element.ajv.keyword.get)
1.  [function <span class="apidocSignatureSpan">ajv.keyword.</span>remove (keyword)](#apidoc.element.ajv.keyword.remove)

#### [module ajv.v5](#apidoc.module.ajv.v5)
1.  [function <span class="apidocSignatureSpan">ajv.v5.</span>enable (ajv)](#apidoc.element.ajv.v5.enable)
1.  string <span class="apidocSignatureSpan">ajv.v5.</span>META_SCHEMA_ID



# <a name="apidoc.module.ajv"></a>[module ajv](#apidoc.module.ajv)

#### <a name="apidoc.element.ajv.ValidationError"></a>[function <span class="apidocSignatureSpan">ajv.</span>ValidationError (errors)](#apidoc.element.ajv.ValidationError)
- description and source-code
```javascript
function ValidationError(errors) {
  this.message = 'validation failed';
  this.errors = errors;
  this.ajv = this.validation = true;
}
```
- example usage
```shell
...

You can define custom formats and keywords that perform validation asyncronously by accessing database or some service. You should
 add 'async: true' in the keyword or format defnition (see [addFormat](#api-addformat), [addKeyword](#api-addkeyword) and [Defining
 custom keywords](#defining-custom-keywords)).

If your schema uses asynchronous formats/keywords or refers to some schema that contains them it should have '"$async": true' keyword
 so that Ajv can compile it correctly. If asynchronous format/keyword or reference to asynchronous schema is used in the schema
without '$async' keyword Ajv will throw an exception during schema compilation.

__Please note__: all asynchronous subschemas that are referenced from the current or other schemas should have '"$async": true'
keyword as well, otherwise the schema compilation will fail.

Validation function for an asynchronous custom format/keyword should return a promise that resolves to 'true' or 'false' (or rejects
 with 'new Ajv.ValidationError(errors)' if you want to return custom errors from the keyword function). Ajv compiles asynchronous
 schemas to either [generator function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) (
default) that can be optionally transpiled with [regenerator](https://github.com/facebook/regenerator) or to [es7 async function
](http://tc39.github.io/ecmascript-asyncawait/) that can be transpiled with [nodent](https://github.com/MatAtBread/nodent) or with
 regenerator as well. You can also supply any other transpiler as a function. See [Options](#options).

The compiled validation function has '$async: true' property (if the schema is asynchronous), so you can differentiate these functions
 if you are using both syncronous and asynchronous schemas.

If you are using generators, the compiled validation function can be either wrapped with [co](https://github.com/tj/co) (default
) or returned as generator function, that can be used directly, e.g. in [koa](http://koajs.com/) 1.0. 'co' is a small library, it
 is included in Ajv (both as npm dependency and in the browser bundle).

Generator functions are currently supported in Chrome, Firefox and node.js (0.11+); if you are using Ajv in other browsers or in
 older versions of node.js you should use one of available transpiling options. All provided async modes use global Promise class
. If your platform does not have Promise you should use a polyfill that defines it.
...
```

#### <a name="apidoc.element.ajv.cache"></a>[function <span class="apidocSignatureSpan">ajv.</span>cache ()](#apidoc.element.ajv.cache)
- description and source-code
```javascript
function Cache() {
  this._cache = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ajv.ValidationError"></a>[module ajv.ValidationError](#apidoc.module.ajv.ValidationError)

#### <a name="apidoc.element.ajv.ValidationError.ValidationError"></a>[function <span class="apidocSignatureSpan">ajv.</span>ValidationError (errors)](#apidoc.element.ajv.ValidationError.ValidationError)
- description and source-code
```javascript
function ValidationError(errors) {
  this.message = 'validation failed';
  this.errors = errors;
  this.ajv = this.validation = true;
}
```
- example usage
```shell
...

You can define custom formats and keywords that perform validation asyncronously by accessing database or some service. You should
 add 'async: true' in the keyword or format defnition (see [addFormat](#api-addformat), [addKeyword](#api-addkeyword) and [Defining
 custom keywords](#defining-custom-keywords)).

If your schema uses asynchronous formats/keywords or refers to some schema that contains them it should have '"$async": true' keyword
 so that Ajv can compile it correctly. If asynchronous format/keyword or reference to asynchronous schema is used in the schema
without '$async' keyword Ajv will throw an exception during schema compilation.

__Please note__: all asynchronous subschemas that are referenced from the current or other schemas should have '"$async": true'
keyword as well, otherwise the schema compilation will fail.

Validation function for an asynchronous custom format/keyword should return a promise that resolves to 'true' or 'false' (or rejects
 with 'new Ajv.ValidationError(errors)' if you want to return custom errors from the keyword function). Ajv compiles asynchronous
 schemas to either [generator function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) (
default) that can be optionally transpiled with [regenerator](https://github.com/facebook/regenerator) or to [es7 async function
](http://tc39.github.io/ecmascript-asyncawait/) that can be transpiled with [nodent](https://github.com/MatAtBread/nodent) or with
 regenerator as well. You can also supply any other transpiler as a function. See [Options](#options).

The compiled validation function has '$async: true' property (if the schema is asynchronous), so you can differentiate these functions
 if you are using both syncronous and asynchronous schemas.

If you are using generators, the compiled validation function can be either wrapped with [co](https://github.com/tj/co) (default
) or returned as generator function, that can be used directly, e.g. in [koa](http://koajs.com/) 1.0. 'co' is a small library, it
 is included in Ajv (both as npm dependency and in the browser bundle).

Generator functions are currently supported in Chrome, Firefox and node.js (0.11+); if you are using Ajv in other browsers or in
 older versions of node.js you should use one of available transpiling options. All provided async modes use global Promise class
. If your platform does not have Promise you should use a polyfill that defines it.
...
```



# <a name="apidoc.module.ajv.ValidationError.prototype"></a>[module ajv.ValidationError.prototype](#apidoc.module.ajv.ValidationError.prototype)

#### <a name="apidoc.element.ajv.ValidationError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">ajv.ValidationError.prototype.</span>constructor (errors)](#apidoc.element.ajv.ValidationError.prototype.constructor)
- description and source-code
```javascript
function ValidationError(errors) {
  this.message = 'validation failed';
  this.errors = errors;
  this.ajv = this.validation = true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ajv.async"></a>[module ajv.async](#apidoc.module.ajv.async)

#### <a name="apidoc.element.ajv.async.compile"></a>[function <span class="apidocSignatureSpan">ajv.async.</span>compile (schema, callback)](#apidoc.element.ajv.async.compile)
- description and source-code
```javascript
function compileAsync(schema, callback) {
<span class="apidocCodeCommentSpan">  /* eslint no-shadow: 0 */
</span>  /* jshint validthis: true */
  var schemaObj;
  var self = this;
  try {
    schemaObj = this._addSchema(schema);
  } catch(e) {
    setTimeout(function() { callback(e); });
    return;
  }
  if (schemaObj.validate) {
    setTimeout(function() { callback(null, schemaObj.validate); });
  } else {
    if (typeof this._opts.loadSchema != 'function')
      throw new Error('options.loadSchema should be a function');
    _compileAsync(schema, callback, true);
  }


  function _compileAsync(schema, callback, firstCall) {
    var validate;
    try { validate = self.compile(schema); }
    catch(e) {
      if (e.missingSchema) loadMissingSchema(e);
      else deferCallback(e);
      return;
    }
    deferCallback(null, validate);

    function loadMissingSchema(e) {
      var ref = e.missingSchema;
      if (self._refs[ref] || self._schemas[ref])
        return callback(new Error('Schema ' + ref + ' is loaded but ' + e.missingRef + ' cannot be resolved'));
      var _callbacks = self._loadingSchemas[ref];
      if (_callbacks) {
        if (typeof _callbacks == 'function')
          self._loadingSchemas[ref] = [_callbacks, schemaLoaded];
        else
          _callbacks[_callbacks.length] = schemaLoaded;
      } else {
        self._loadingSchemas[ref] = schemaLoaded;
        self._opts.loadSchema(ref, function (err, sch) {
          var _callbacks = self._loadingSchemas[ref];
          delete self._loadingSchemas[ref];
          if (typeof _callbacks == 'function') {
            _callbacks(err, sch);
          } else {
            for (var i=0; i<_callbacks.length; i++)
              _callbacks[i](err, sch);
          }
        });
      }

      function schemaLoaded(err, sch) {
        if (err) return callback(err);
        if (!(self._refs[ref] || self._schemas[ref])) {
          try {
            self.addSchema(sch, ref);
          } catch(e) {
            callback(e);
            return;
          }
        }
        _compileAsync(schema, callback);
      }
    }

    function deferCallback(err, validate) {
      if (firstCall) setTimeout(function() { callback(err, validate); });
      else return callback(err, validate);
    }
  }
}
```
- example usage
```shell
...


The fastest validation call:

'''javascript
var Ajv = require('ajv');
var ajv = new Ajv(); // options can be passed, e.g. {allErrors: true}
var validate = ajv.compile(schema);
var valid = validate(data);
if (!valid) console.log(validate.errors);
'''

or with less code

'''javascript
...
```

#### <a name="apidoc.element.ajv.async.setup"></a>[function <span class="apidocSignatureSpan">ajv.async.</span>setup (opts, required)](#apidoc.element.ajv.async.setup)
- description and source-code
```javascript
function setupAsync(opts, required) {
  if (required !== false) required = true;
  var async = opts.async
    , transpile = opts.transpile
    , check;

  switch (typeof transpile) {
    case 'string':
      var get = TRANSPILE[transpile];
      if (!get) throw new Error('bad transpiler: ' + transpile);
      return (opts._transpileFunc = get(opts, required));
    case 'undefined':
    case 'boolean':
      if (typeof async == 'string') {
        check = ASYNC[async];
        if (!check) throw new Error('bad async mode: ' + async);
        return (opts.transpile = check(opts, required));
      }

      for (var i=0; i<MODES.length; i++) {
        var _opts = MODES[i];
        if (setupAsync(_opts, false)) {
          util.copy(_opts, opts);
          return opts.transpile;
        }
      }
<span class="apidocCodeCommentSpan">      /* istanbul ignore next */
</span>      throw new Error('generators, nodent and regenerator are not available');
    case 'function':
      return (opts._transpileFunc = opts.transpile);
    default:
      throw new Error('bad transpiler: ' + transpile);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ajv.cache"></a>[module ajv.cache](#apidoc.module.ajv.cache)

#### <a name="apidoc.element.ajv.cache.cache"></a>[function <span class="apidocSignatureSpan">ajv.</span>cache ()](#apidoc.element.ajv.cache.cache)
- description and source-code
```javascript
function Cache() {
  this._cache = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ajv.cache.prototype"></a>[module ajv.cache.prototype](#apidoc.module.ajv.cache.prototype)

#### <a name="apidoc.element.ajv.cache.prototype.clear"></a>[function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>clear ()](#apidoc.element.ajv.cache.prototype.clear)
- description and source-code
```javascript
function Cache_clear() {
  this._cache = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ajv.cache.prototype.del"></a>[function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>del (key)](#apidoc.element.ajv.cache.prototype.del)
- description and source-code
```javascript
function Cache_del(key) {
  delete this._cache[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ajv.cache.prototype.get"></a>[function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>get (key)](#apidoc.element.ajv.cache.prototype.get)
- description and source-code
```javascript
function Cache_get(key) {
  return this._cache[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ajv.cache.prototype.put"></a>[function <span class="apidocSignatureSpan">ajv.cache.prototype.</span>put (key, value)](#apidoc.element.ajv.cache.prototype.put)
- description and source-code
```javascript
function Cache_put(key, value) {
  this._cache[key] = value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ajv.keyword"></a>[module ajv.keyword](#apidoc.module.ajv.keyword)

#### <a name="apidoc.element.ajv.keyword.add"></a>[function <span class="apidocSignatureSpan">ajv.keyword.</span>add (keyword, definition)](#apidoc.element.ajv.keyword.add)
- description and source-code
```javascript
function addKeyword(keyword, definition) {
<span class="apidocCodeCommentSpan">  /* jshint validthis: true */
</span>  /* eslint no-shadow: 0 */
  var RULES = this.RULES;

  if (RULES.keywords[keyword])
    throw new Error('Keyword ' + keyword + ' is already defined');

  if (!IDENTIFIER.test(keyword))
    throw new Error('Keyword ' + keyword + ' is not a valid identifier');

  if (definition) {
    if (definition.macro && definition.valid !== undefined)
      throw new Error('"valid" option cannot be used with macro keywords');

    var dataType = definition.type;
    if (Array.isArray(dataType)) {
      var i, len = dataType.length;
      for (i=0; i<len; i++) checkDataType(dataType[i]);
      for (i=0; i<len; i++) _addRule(keyword, dataType[i], definition);
    } else {
      if (dataType) checkDataType(dataType);
      _addRule(keyword, dataType, definition);
    }

    var $data = definition.$data === true && this._opts.v5;
    if ($data && !definition.validate)
      throw new Error('$data support: "validate" function is not defined');

    var metaSchema = definition.metaSchema;
    if (metaSchema) {
      if ($data) {
        metaSchema = {
          anyOf: [
            metaSchema,
            { '$ref': 'https://raw.githubusercontent.com/epoberezkin/ajv/master/lib/refs/json-schema-v5.json#/definitions/$data' }
          ]
        };
      }
      definition.validateSchema = this.compile(metaSchema, true);
    }
  }

  RULES.keywords[keyword] = RULES.all[keyword] = true;


  function _addRule(keyword, dataType, definition) {
    var ruleGroup;
    for (var i=0; i<RULES.length; i++) {
      var rg = RULES[i];
      if (rg.type == dataType) {
        ruleGroup = rg;
        break;
      }
    }

    if (!ruleGroup) {
      ruleGroup = { type: dataType, rules: [] };
      RULES.push(ruleGroup);
    }

    var rule = {
      keyword: keyword,
      definition: definition,
      custom: true,
      code: customRuleCode
    };
    ruleGroup.rules.push(rule);
    RULES.custom[keyword] = rule;
  }


  function checkDataType(dataType) {
    if (!RULES.types[dataType]) throw new Error('Unknown type ' + dataType);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ajv.keyword.get"></a>[function <span class="apidocSignatureSpan">ajv.keyword.</span>get (keyword)](#apidoc.element.ajv.keyword.get)
- description and source-code
```javascript
function getKeyword(keyword) {
<span class="apidocCodeCommentSpan">  /* jshint validthis: true */
</span>  var rule = this.RULES.custom[keyword];
  return rule ? rule.definition : this.RULES.keywords[keyword] || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ajv.keyword.remove"></a>[function <span class="apidocSignatureSpan">ajv.keyword.</span>remove (keyword)](#apidoc.element.ajv.keyword.remove)
- description and source-code
```javascript
function removeKeyword(keyword) {
<span class="apidocCodeCommentSpan">  /* jshint validthis: true */
</span>  var RULES = this.RULES;
  delete RULES.keywords[keyword];
  delete RULES.all[keyword];
  delete RULES.custom[keyword];
  for (var i=0; i<RULES.length; i++) {
    var rules = RULES[i].rules;
    for (var j=0; j<rules.length; j++) {
      if (rules[j].keyword == keyword) {
        rules.splice(j, 1);
        break;
      }
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.ajv.v5"></a>[module ajv.v5](#apidoc.module.ajv.v5)

#### <a name="apidoc.element.ajv.v5.enable"></a>[function <span class="apidocSignatureSpan">ajv.v5.</span>enable (ajv)](#apidoc.element.ajv.v5.enable)
- description and source-code
```javascript
function enableV5(ajv) {
  var inlineFunctions = {
    'switch': require('./dotjs/switch'),
    'constant': require('./dotjs/constant'),
    '_formatLimit': require('./dotjs/_formatLimit'),
    'patternRequired': require('./dotjs/patternRequired')
  };

  if (ajv._opts.meta !== false) {
    var metaSchema = require('./refs/json-schema-v5.json');
    ajv.addMetaSchema(metaSchema, META_SCHEMA_ID);
  }
  _addKeyword('constant');
  ajv.addKeyword('contains', { type: 'array', macro: containsMacro });

  _addKeyword('formatMaximum', 'string', inlineFunctions._formatLimit);
  _addKeyword('formatMinimum', 'string', inlineFunctions._formatLimit);
  ajv.addKeyword('formatExclusiveMaximum');
  ajv.addKeyword('formatExclusiveMinimum');

  ajv.addKeyword('patternGroups'); // implemented in properties.jst
  _addKeyword('patternRequired', 'object');
  _addKeyword('switch');


  function _addKeyword(keyword, types, inlineFunc) {
    var definition = {
      inline: inlineFunc || inlineFunctions[keyword],
      statements: true,
      errors: 'full'
    };
    if (types) definition.type = types;
    ajv.addKeyword(keyword, definition);
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
