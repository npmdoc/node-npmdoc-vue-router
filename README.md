# api documentation for  [vue-router (v2.3.1)](https://github.com/vuejs/vue-router#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-vue-router.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-vue-router) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-vue-router.svg)](https://travis-ci.org/npmdoc/node-npmdoc-vue-router)
#### Official router for Vue.js 2

[![NPM](https://nodei.co/npm/vue-router.png?downloads=true)](https://www.npmjs.com/package/vue-router)

[![apidoc](https://npmdoc.github.io/node-npmdoc-vue-router/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-vue-router_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-vue-router/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-vue-router/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-vue-router/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Evan You"
    },
    "bugs": {
        "url": "https://github.com/vuejs/vue-router/issues"
    },
    "dependencies": {},
    "description": "Official router for Vue.js 2",
    "devDependencies": {
        "babel-core": "^6.11.4",
        "babel-eslint": "^7.1.1",
        "babel-loader": "^6.2.4",
        "babel-plugin-syntax-dynamic-import": "^6.18.0",
        "babel-preset-es2015": "^6.9.0",
        "babel-preset-es2015-loose": "^8.0.0",
        "babel-preset-flow-vue": "^1.0.0",
        "buble": "^0.15.2",
        "chromedriver": "^2.21.2",
        "cross-spawn": "^5.0.1",
        "css-loader": "^0.26.1",
        "es6-promise": "^4.0.5",
        "eslint": "^3.0.1",
        "eslint-config-vue": "^2.0.1",
        "eslint-plugin-flow-vars": "^0.5.0",
        "eslint-plugin-vue": "^2.0.1",
        "express": "^4.14.0",
        "express-urlrewrite": "^1.2.0",
        "flow-bin": "^0.40.0",
        "gitbook-plugin-edit-link": "^2.0.2",
        "gitbook-plugin-github": "^3.0.0",
        "jasmine": "2.5.3",
        "nightwatch": "^0.9.5",
        "nightwatch-helpers": "^1.0.0",
        "path-to-regexp": "^1.5.3",
        "phantomjs-prebuilt": "^2.1.7",
        "rollup": "^0.41.4",
        "rollup-plugin-buble": "^0.15.0",
        "rollup-plugin-commonjs": "^7.0.0",
        "rollup-plugin-flow-no-whitespace": "^1.0.0",
        "rollup-plugin-node-resolve": "^2.0.0",
        "rollup-plugin-replace": "^1.1.1",
        "rollup-watch": "^3.2.2",
        "selenium-server": "^2.53.1",
        "typescript": "^2.0.3",
        "uglify-js": "^2.7.0",
        "vue": "^2.1.0",
        "vue-loader": "^11.0.0",
        "vue-template-compiler": "^2.1.0",
        "webpack": "^2.2.0",
        "webpack-dev-middleware": "^1.9.0"
    },
    "directories": {},
    "dist": {
        "shasum": "3135448cf57d4ca576906061a5a9d25fae0214d7",
        "tarball": "https://registry.npmjs.org/vue-router/-/vue-router-2.3.1.tgz"
    },
    "files": [
        "src",
        "dist/*.js",
        "types/*.d.ts"
    ],
    "gitHead": "a1de424211446006e7abd6d478b00d41ae609f81",
    "homepage": "https://github.com/vuejs/vue-router#readme",
    "keywords": [
        "vue",
        "router",
        "routing"
    ],
    "license": "MIT",
    "main": "dist/vue-router.common.js",
    "maintainers": [
        {
            "name": "yyx990803",
            "email": "yyx990803@gmail.com"
        }
    ],
    "module": "dist/vue-router.esm.js",
    "name": "vue-router",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/vuejs/vue-router.git"
    },
    "scripts": {
        "build": "node build/build.js",
        "dev": "node examples/server.js",
        "dev:dist": "rollup -wm -c build/dev.config.js",
        "docs": "cd docs && gitbook install && gitbook serve",
        "docs:deploy": "bash ./build/update-docs.sh",
        "lint": "eslint src examples",
        "release": "bash build/release.sh",
        "test": "npm run lint && flow check && npm run test:unit && npm run test:e2e && npm run test:types",
        "test:e2e": "node test/e2e/runner.js",
        "test:types": "tsc -p types/test",
        "test:unit": "jasmine JASMINE_CONFIG_PATH=test/unit/jasmine.json"
    },
    "typings": "types/index.d.ts",
    "unpkg": "dist/vue-router.js",
    "version": "2.3.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module vue-router](#apidoc.module.vue-router)
1.  [function <span class="apidocSignatureSpan">vue-router.</span>install (Vue)](#apidoc.element.vue-router.install)
1.  string <span class="apidocSignatureSpan">vue-router.</span>version



# <a name="apidoc.module.vue-router"></a>[module vue-router](#apidoc.module.vue-router)

#### <a name="apidoc.element.vue-router.install"></a>[function <span class="apidocSignatureSpan">vue-router.</span>install (Vue)](#apidoc.element.vue-router.install)
- description and source-code
```javascript
function install(Vue) {
  if (install.installed) { return }
  install.installed = true;

  _Vue = Vue;

  Object.defineProperty(Vue.prototype, '$router', {
    get: function get () { return this.$root._router }
  });

  Object.defineProperty(Vue.prototype, '$route', {
    get: function get () { return this.$root._route }
  });

  Vue.mixin({
    beforeCreate: function beforeCreate () {
      if (this.$options.router) {
        this._router = this.$options.router;
        this._router.init(this);
        Vue.util.defineReactive(this, '_route', this._router.history.current);
      }
    }
  });

  Vue.component('router-view', View);
  Vue.component('router-link', Link);

  var strats = Vue.config.optionMergeStrategies;
  // use the same hook merging strategy for route hooks
  strats.beforeRouteEnter = strats.beforeRouteLeave = strats.created;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
