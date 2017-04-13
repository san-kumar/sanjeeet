# Innovate Frontend Admin

## About
A Webpack Angular kit featuring:
* AngularJS (setup, angular-material, router, ...)
* [TypeScript](http://www.typescriptlang.org/)
  * the future of JavaScript available now
* [Redux](https://github.com/rackt/redux)
  * one-way data flow for shared state management
* [Immutable.js](https://facebook.github.io/immutable-js/)
* [RxJS](https://github.com/Reactive-Extensions/RxJS)
* [Lodash](https://lodash.com/)
* [PostCSS](https://github.com/postcss/postcss)
* [Autoprefixer](https://github.com/postcss/autoprefixer)
* [Karma](http://karma-runner.github.io/)
  * unit test runner
* [Protractor](https://angular.github.io/protractor/#/)
  * end-to-end test framework/runner
* [Jasmine](http://jasmine.github.io/)
  * bdd unit testing library
* [Istanbul](https://gotwarlost.github.io/istanbul/)
  * generate code coverage reports
* [TSLint](https://www.npmjs.com/package/tslint)
  * check TypeScript code quality/style
* [Typings](https://github.com/typings/typings)
  * manage TypeScript type definitions
* [TSDoc](https://www.npmjs.com/package/tsdoc)
  * generate API documentation
* [moment](http://momentjs.com/)
* [Sinon.JS](http://sinonjs.org/)
* [SASS](http://sass-lang.com/)
* [JSData](http://www.js-data.io/)

A complete build based on Webpack/npm scripts and tons of features:
* hot module replacement (HMR)
  * https://webpack.github.io/docs/hot-module-replacement-with-webpack.html
  * https://webpack.github.io/docs/hot-module-replacement.html
  * http://andrewhfarmer.com/understanding-hmr/
  * http://andrewhfarmer.com/why-use-hmr/
* unit tests (Karma & Jasmine)
* end to end tests (Protractor)
* test coverage reports (Istanbul)
  * html, lcov, junit
* TS to ES5 transpilation (TypeScript)
* SASS to CSS transpilation (SASS)
* TS quality/style checks (TSLint)
* TS code documentation generation (TSDoc)
* development and production configurations
  * optimizations for production (minification, compression, ...)
* security best practices applied to dev server configuration
  * Content Security Policy (CSP)
  * Other security headers
* ...

## Installation
First of all, make sure that you have installed NodeJS & npm: https://nodejs.org/en/.

Two approaches:
* clone this repository: `git clone https://github.com/InnovateMRLLC/frontend_admin.git`
* download a zip: https://github.com/InnovateMRLLC/frontend_admin/archive/master.zip

Now you can download all the necessary dependencies using the setup script: `npm run setup`.

Finally, you can start the development server using `npm start`.

Check out the scripts section below for more information about the available commands.

## Scripts
* `npm run setup`: install required global dependencies and project dependencies
* `npm start`: start the development server with Hot Module Replacement (HMR) and live reloading
* `npm run start:hmr`: start the development server with Hot Module Replacement enabled but without live reloading (e.g., no automatic reload when stylesheets change)
* `npm run start:hmr:livereload`: start the development server with Hot Module Replacement (HMR) and live reloading
* `npm run build:prod`: build the production version (in /dist)
* `npm run start:prod`: build and serve the production version
* `npm run profiling`: generate Webpack profiling information under `reports/profiling`. The stats.json file can be uploaded to http://webpack.github.io/analyse/ for analysis
* `npm test`: run unit tests
* `npm run test-subset src/?`: run a subset of the unit tests where ? is either a specific file or a folder. Only tests matching the given path will be executed. The given path MUST start with src/. The file name (if any specified) MUST contain the file extension
  * example: `npm run test-subset src/app/tests/sanity_test_spec.ts`
* `npm run e2e`: run end to end tests
* `npm run e2e:live`: run end to end tests in debug mode: https://github.com/angular/protractor/blob/master/docs/debugging.md
* `npm run ci`: run unit tests and integration tests
* `npm run clean`: clean generated folders and files
* `npm run clean:all`: clean + remove installed TypeScript type definitions + npm clean
* `npm run clean:dist`: only clean the dist folder
* `npm run clean:install`: clean all + remove installed node_modules + install
* `npm run clean:start`: clean + start the development server
* `npm run docs`: generate documentation
* `npm run lint`: lint TypeScript code
* `npm run outdated`: check for outdated dependencies
* `npm run superstatic`: starts the production server (assumes that you've executed `npm run build:prod` before)
* `npm run tsc`: run the TypeScript compiler
* `npm run typings-install`: install TypeScript type definitions using typings
* `npm run watch`: start the development webpack build in watch mode
* `npm run watch:prod`: start the production webpack build in watch mode
* `npm run watch:test`: start the test webpack build in watch mode
* `npm run watch:test-subset`: start the test webpack build in watch mode and filter the tests to execute (see npm test)
* `npm run watch:testd`: start the test webpack build in watch mode with debugging enabled
* `npm run webdriver:start`: start the Webdriver Manager
* `npm run webdriver:update`: update Webdriver

### Production server
The production server that you can start via `npm run server:prod` uses Superstatic (https://github.com/firebase/superstatic).
It is configured via `superstatic.json` to enable support for push-state (HTML 5 mode)
