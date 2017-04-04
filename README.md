# api documentation for  [eslint-plugin-import (v2.2.0)](https://github.com/benmosher/eslint-plugin-import)  [![npm package](https://img.shields.io/npm/v/npmdoc-eslint-plugin-import.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-eslint-plugin-import) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-eslint-plugin-import.svg)](https://travis-ci.org/npmdoc/node-npmdoc-eslint-plugin-import)
#### Import with sanity.

[![NPM](https://nodei.co/npm/eslint-plugin-import.png?downloads=true)](https://www.npmjs.com/package/eslint-plugin-import)

[![apidoc](https://npmdoc.github.io/node-npmdoc-eslint-plugin-import/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-eslint-plugin-import_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-eslint-plugin-import/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-eslint-plugin-import/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-eslint-plugin-import/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ben Mosher",
        "email": "me@benmosher.com"
    },
    "bugs": {
        "url": "https://github.com/benmosher/eslint-plugin-import/issues"
    },
    "dependencies": {
        "builtin-modules": "^1.1.1",
        "contains-path": "^0.1.0",
        "debug": "^2.2.0",
        "doctrine": "1.5.0",
        "eslint-import-resolver-node": "^0.2.0",
        "eslint-module-utils": "^2.0.0",
        "has": "^1.0.1",
        "lodash.cond": "^4.3.0",
        "minimatch": "^3.0.3",
        "pkg-up": "^1.0.0"
    },
    "description": "Import with sanity.",
    "devDependencies": {
        "babel-eslint": "next",
        "babel-plugin-istanbul": "^2.0.1",
        "babel-preset-es2015-argon": "latest",
        "babel-register": "6.16.3",
        "chai": "^3.4.0",
        "coveralls": "^2.11.4",
        "cross-env": "^3.1.0",
        "eslint": "3.x",
        "eslint-import-resolver-node": "file:./resolvers/node",
        "eslint-import-resolver-webpack": "file:./resolvers/webpack",
        "eslint-module-utils": "file:./utils",
        "eslint-plugin-import": "2.x",
        "gulp": "^3.9.0",
        "gulp-babel": "6.1.2",
        "istanbul": "^0.4.0",
        "linklocal": "^2.6.0",
        "mocha": "^3.1.2",
        "nyc": "^8.3.0",
        "redux": "^3.0.4",
        "rimraf": "2.5.2",
        "typescript": "^2.0.3",
        "typescript-eslint-parser": "^0.4.0"
    },
    "directories": {
        "test": "tests"
    },
    "dist": {
        "shasum": "72ba306fad305d67c4816348a4699a4229ac8b4e",
        "tarball": "https://registry.npmjs.org/eslint-plugin-import/-/eslint-plugin-import-2.2.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "lib",
        "config",
        "memo-parser"
    ],
    "gitHead": "90ef48b3ade57c77526b285f75dc0cfc41537831",
    "homepage": "https://github.com/benmosher/eslint-plugin-import",
    "keywords": [
        "eslint",
        "eslintplugin",
        "es6",
        "jsnext",
        "modules",
        "import",
        "export"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "benmosher",
            "email": "me@benmosher.com"
        }
    ],
    "name": "eslint-plugin-import",
    "nyc": {
        "require": [
            "babel-register"
        ],
        "sourceMap": false,
        "instrument": false
    },
    "optionalDependencies": {},
    "peerDependencies": {
        "eslint": "2.x - 3.x"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/benmosher/eslint-plugin-import.git"
    },
    "scripts": {
        "ci-test": "eslint ./src && gulp pretest && cross-env NODE_PATH=./lib istanbul cover --report lcovonly --dir reports/coverage _mocha tests/lib/ -- --recursive --reporter dot",
        "cover": "gulp pretest && cross-env NODE_PATH=./lib istanbul cover --dir reports/coverage _mocha tests/lib/ -- --recursive -R progress",
        "coverage-report": "npm t && nyc report --reporter html",
        "coveralls": "nyc report --reporter lcovonly && cat ./coverage/lcov.info | coveralls",
        "debug": "cross-env NODE_PATH=./lib mocha debug --recursive --reporter dot tests/lib/",
        "posttest": "eslint ./src",
        "prepublish": "gulp prepublish",
        "pretest": "linklocal",
        "test": "cross-env BABEL_ENV=test NODE_PATH=./src nyc -s mocha -R dot --recursive tests/src -t 5s",
        "test-all": "npm test && for resolver in ./resolvers/*; do cd $resolver && npm test && cd ../..; done",
        "test-compiled": "npm run prepublish && NODE_PATH=./lib mocha --compilers js:babel-register --recursive tests/src",
        "watch": "cross-env NODE_PATH=./src mocha --watch --compilers js:babel-register --recursive tests/src"
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module eslint-plugin-import](#apidoc.module.eslint-plugin-import)
1.  object <span class="apidocSignatureSpan">eslint-plugin-import.</span>ExportMap
1.  object <span class="apidocSignatureSpan">eslint-plugin-import.</span>configs
1.  object <span class="apidocSignatureSpan">eslint-plugin-import.</span>importDeclaration
1.  object <span class="apidocSignatureSpan">eslint-plugin-import.</span>rules

#### [module eslint-plugin-import.ExportMap](#apidoc.module.eslint-plugin-import.ExportMap)
1.  [function <span class="apidocSignatureSpan">eslint-plugin-import.ExportMap.</span>default (path)](#apidoc.element.eslint-plugin-import.ExportMap.default)
1.  [function <span class="apidocSignatureSpan">eslint-plugin-import.ExportMap.</span>recursivePatternCapture (pattern, callback)](#apidoc.element.eslint-plugin-import.ExportMap.recursivePatternCapture)

#### [module eslint-plugin-import.importDeclaration](#apidoc.module.eslint-plugin-import.importDeclaration)
1.  [function <span class="apidocSignatureSpan">eslint-plugin-import.importDeclaration.</span>default (context)](#apidoc.element.eslint-plugin-import.importDeclaration.default)



# <a name="apidoc.module.eslint-plugin-import"></a>[module eslint-plugin-import](#apidoc.module.eslint-plugin-import)



# <a name="apidoc.module.eslint-plugin-import.ExportMap"></a>[module eslint-plugin-import.ExportMap](#apidoc.module.eslint-plugin-import.ExportMap)

#### <a name="apidoc.element.eslint-plugin-import.ExportMap.default"></a>[function <span class="apidocSignatureSpan">eslint-plugin-import.ExportMap.</span>default (path)](#apidoc.element.eslint-plugin-import.ExportMap.default)
- description and source-code
```javascript
class ExportMap {
  constructor(path) {
    this.path = path;
    this.namespace = new Map();
    // todo: restructure to key on path, value is resolver + map of names
    this.reexports = new Map();
    this.dependencies = new Map();
    this.errors = [];
  }

  get hasDefault() {
    return this.get('default') != null;
  } // stronger than this.has

  get size() {
    let size = this.namespace.size + this.reexports.size;
    this.dependencies.forEach(dep => size += dep().size);
    return size;
  }

<span class="apidocCodeCommentSpan">  /**
   * Note that this does not check explicitly re-exported names for existence
   * in the base namespace, but it will expand all 'export * from '...'' exports
   * if not found in the explicit namespace.
   * @param  {string}  name
   * @return {Boolean} true if 'name' is exported by this module.
   */
</span>  has(name) {
    if (this.namespace.has(name)) return true;
    if (this.reexports.has(name)) return true;

    // default exports must be explicitly re-exported (#328)
    if (name !== 'default') {
      for (let dep of this.dependencies.values()) {
        let innerMap = dep();

        // todo: report as unresolved?
        if (!innerMap) continue;

        if (innerMap.has(name)) return true;
      }
    }

    return false;
  }

  /**
   * ensure that imported name fully resolves.
   * @param  {[type]}  name [description]
   * @return {Boolean}      [description]
   */
  hasDeep(name) {
    if (this.namespace.has(name)) return { found: true, path: [this] };

    if (this.reexports.has(name)) {
      const reexports = this.reexports.get(name),
            imported = reexports.getImport();

      // if import is ignored, return explicit 'null'
      if (imported == null) return { found: true, path: [this] };

      // safeguard against cycles, only if name matches
      if (imported.path === this.path && reexports.local === name) {
        return { found: false, path: [this] };
      }

      const deep = imported.hasDeep(reexports.local);
      deep.path.unshift(this);

      return deep;
    }

    // default exports must be explicitly re-exported (#328)
    if (name !== 'default') {
      for (let dep of this.dependencies.values()) {
        let innerMap = dep();
        // todo: report as unresolved?
        if (!innerMap) continue;

        // safeguard against cycles
        if (innerMap.path === this.path) continue;

        let innerValue = innerMap.hasDeep(name);
        if (innerValue.found) {
          innerValue.path.unshift(this);
          return innerValue;
        }
      }
    }

    return { found: false, path: [this] };
  }

  get(name) {
    if (this.namespace.has(name)) return this.namespace.get(name);

    if (this.reexports.has(name)) {
      const reexports = this.reexports.get(name),
            imported = reexports.getImport();

      // if import is ignored, return explicit 'null'
      if (imported == null) return null;

      // safeguard against cycles, only if name matches
      if (imported.path === this.path && reexports.local === name) return undefined;

      return imported.get(reexports.local);
    }

    // default exports must be explicitly re-exported (#328)
    if (name !== 'default') {
      for (let dep of this.dependencies.values()) {
        let innerMap = dep();
        // todo: report as unresolved?
        if (!innerMap) continue;

        // safeguard against cycles
        if (innerMap.path === this.path) continue;

        let innerValue = innerMap.get(name);
        if (innerValue !== undefined) return innerValue;
      }
    }

    return undefined;
  }

  forEach(callback, thisArg) {
    this.namespace.forEach((v, n) => callback.call(thisArg, v, n, this));

    this.reexports.forEach((reexports, name) => {
      const reexported = reexports.getImport();
      // can't look up meta for ignored re-exports (#348)
      callback.call(thisArg, reexported && reexported.get(reexports.local), name, this);
    });

    this.dependencies.forEach(dep => dep().forEach((v, n) => n !== 'default' && callback.call(thisArg, v, n, this)));
  }

  // todo: keys, values, entries? ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.eslint-plugin-import.ExportMap.recursivePatternCapture"></a>[function <span class="apidocSignatureSpan">eslint-plugin-import.ExportMap.</span>recursivePatternCapture (pattern, callback)](#apidoc.element.eslint-plugin-import.ExportMap.recursivePatternCapture)
- description and source-code
```javascript
function recursivePatternCapture(pattern, callback) {
  switch (pattern.type) {
    case 'Identifier':
      // base case
      callback(pattern);
      break;

    case 'ObjectPattern':
      pattern.properties.forEach(p => {
        recursivePatternCapture(p.value, callback);
      });
      break;

    case 'ArrayPattern':
      pattern.elements.forEach(element => {
        if (element == null) return;
        recursivePatternCapture(element, callback);
      });
      break;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.eslint-plugin-import.importDeclaration"></a>[module eslint-plugin-import.importDeclaration](#apidoc.module.eslint-plugin-import.importDeclaration)

#### <a name="apidoc.element.eslint-plugin-import.importDeclaration.default"></a>[function <span class="apidocSignatureSpan">eslint-plugin-import.importDeclaration.</span>default (context)](#apidoc.element.eslint-plugin-import.importDeclaration.default)
- description and source-code
```javascript
function importDeclaration(context) {
  var ancestors = context.getAncestors();
  return ancestors[ancestors.length - 1];
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
