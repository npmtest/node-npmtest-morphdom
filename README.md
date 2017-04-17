# test coverage for  [morphdom (v2.3.2)](https://github.com/patrick-steele-idem/morphdom#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-morphdom.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-morphdom) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-morphdom.svg)](https://travis-ci.org/npmtest/node-npmtest-morphdom)
#### Morph a DOM tree to another DOM tree (no virtual DOM needed)

[![NPM](https://nodei.co/npm/morphdom.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/morphdom)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-morphdom/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-morphdom/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-morphdom/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-morphdom/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-morphdom/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-morphdom/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-morphdom/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-morphdom/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-morphdom/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-morphdom/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-morphdom/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-morphdom/build/test-report.html](https://npmtest.github.io/node-npmtest-morphdom/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-morphdom/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-morphdom/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-morphdom/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-morphdom/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-morphdom/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-morphdom/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-morphdom/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-morphdom/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Patrick Steele-Idem"
    },
    "bugs": {
        "url": "https://github.com/patrick-steele-idem/morphdom/issues"
    },
    "dependencies": {},
    "description": "Morph a DOM tree to another DOM tree (no virtual DOM needed)",
    "devDependencies": {
        "async": "^2.0.0",
        "browser-refresh-taglib": "^1.1.0",
        "chai": "^2.3.0",
        "diffhtml": "^0.9.2",
        "express": "^4.14.0",
        "ignoring-watcher": "^1.0.5",
        "jshint": "^2.7.0",
        "lasso": "^2.4.1",
        "lasso-marko": "^2.0.7",
        "marko": "^4.1.3",
        "mocha": "^2.2.4",
        "mocha-phantomjs": "^4.1.0",
        "phantomjs-prebuilt": "^2.1.13",
        "rollup": "^0.39.2",
        "uglify-js": "^2.6.2",
        "umd": "^3.0.1",
        "vdom-virtualize": "0.0.12",
        "virtual-dom": "^2.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "6a71001f55e518f06b42e0e1f1084feaf8da2024",
        "tarball": "https://registry.npmjs.org/morphdom/-/morphdom-2.3.2.tgz"
    },
    "gitHead": "43b808008bd39b571a1dd32d49811c7c22bd2021",
    "homepage": "https://github.com/patrick-steele-idem/morphdom#readme",
    "keywords": [
        "dom",
        "diff",
        "patch",
        "virtual",
        "browser"
    ],
    "license": "MIT",
    "main": "dist/morphdom.js",
    "maintainers": [
        {
            "name": "mlrawlings"
        },
        {
            "name": "pnidem"
        }
    ],
    "name": "morphdom",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/patrick-steele-idem/morphdom.git"
    },
    "scripts": {
        "all": "npm run all-browser && npm run lint",
        "all-browser": "node test/mocha-phantomjs/run.js test benchmark",
        "benchmark": "npm run benchmark-browser",
        "benchmark-browser": "node test/mocha-phantomjs/run.js benchmark",
        "build": "npm run rollup && npm run minify",
        "lint": "jshint src/",
        "minify": "uglifyjs ./dist/morphdom-umd.js -o ./dist/morphdom-umd.min.js",
        "mocha-phantomjs": "node test/mocha-phantomjs/run.js",
        "mocha-phantomjs-run": "mocha-phantomjs -p node_modules/.bin/phantomjs ./test/mocha-phantomjs/generated/test-page.html",
        "prepublish": "npm run build",
        "rollup": "npm run rollup-default && npm run rollup-factory && npm run rollup-default-umd",
        "rollup-default": "rollup src/index.js -o dist/morphdom.js --format cjs",
        "rollup-default-umd": "rollup src/index.js -o dist/morphdom-umd.js --format umd --name morphdom",
        "rollup-factory": "rollup src/morphdom.js -o dist/morphdom-factory.js --format cjs",
        "start": "node examples/server.js",
        "test": "npm run build && npm run test-browser && npm run lint",
        "test-browser": "node test/mocha-phantomjs/run.js test"
    },
    "version": "2.3.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
