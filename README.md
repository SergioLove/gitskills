
# gitskills  master

# gitskills  feature  new feature

{
  "name": "vue-router",
  "version": "0.7.13",
  "description": "A router for Vue.js",
  "main": "dist/vue-router.js",
  "jsnext:main": "src/index.js",
  "files": [
    "dist",
    "src",
    "lib"
  ],
  "scripts": {
    "dev": "npm run serve-test & webpack --watch --config build/webpack.dev.config.js",
    "lint": "eslint src build test/e2e test/unit/specs",
    "unit": "./node_modules/karma/bin/karma start build/karma.config.js",
    "build": "node build/build.js",
    "serve-example": "webpack-dev-server --inline --hot --config example/advanced/webpack.config.js --content-base example/advanced --history-api-fallback --host 0.0.0.0",
    "serve-test": "webpack-dev-server --quiet --config test/unit/webpack.config.js --content-base test/unit --history-api-fallback --host 0.0.0.0 --port 8081",
    "e2e-sauce": "nightwatch -c build/nightwatch.sauce.json -e chrome,firefox,ie10,ie11",
    "e2e-local": "bash ./build/e2e.sh",
    "release": "bash ./build/release.sh",
    "docs": "cd docs && gitbook serve",
    "deploy-docs": "bash ./build/update-docs.sh",
    "test": "npm run lint && npm run unit && npm run e2e-local"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/vuejs/vue-router.git"
  },
  "keywords": [
    "vue",
    "vuejs",
    "router",
    "mvvm"
  ],
  "author": "Evan You",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/vuejs/vue-router/issues"
  },
  "homepage": "https://github.com/vuejs/vue-router#readme",
  "devDependencies": {
    "babel-core": "^5.8.33",
    "babel-loader": "^5.3.3",
    "babel-runtime": "^5.8.29",
    "chromedriver": "2.20.0",
    "css-loader": "^0.23.1",
    "es6-promise": "^3.0.2",
    "eslint": "^1.3.1",
    "express": "^4.12.3",
    "istanbul-instrumenter-loader": "^0.1.3",
    "jasmine-core": "^2.3.2",
    "karma": "^0.13.8",
    "karma-coverage": "^0.5.0",
    "karma-jasmine": "^0.3.5",
    "karma-phantomjs-launcher": "^0.2.1",
    "karma-sourcemap-loader": "^0.3.7",
    "karma-spec-reporter": "0.0.23",
    "karma-webpack": "^1.7.0",
    "nightwatch": "^0.8.15",
    "phantomjs": "^1.9.19",
    "rollup": "^0.21.0",
    "rollup-plugin-babel": "^1.0.0",
    "selenium-server": "2.53.0",
    "style-loader": "^0.13.0",
    "uglify-js": "^2.5.0",
    "vue": "^1.0.14",
    "vue-hot-reload-api": "^1.2.1",
    "vue-html-loader": "^1.0.0",
    "vue-loader": "^6.0.3",
    "webpack": "^1.11.0",
    "webpack-dev-server": "^1.10.1"
  },
  "jspm": {
    "main": "src/index.js",
    "registry": "npm",
    "format": "esm"
  }
}
