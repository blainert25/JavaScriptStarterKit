# Java Script Starter Kit

This is a starter kit for any JavaScript development. It was developed using the Pluralsight course [Building a JavaScript Development Environment](https://www.pluralsight.com/courses/javascript-development-environment).

## Editor
This starter kit contains an EditorConfig file which comes with some presets that will make set up easier.

The suggested editor is Visual Studio Code, however EditorConfig has plug-ins for most editors so feel free to use the editor that is most comfortable for you.

For more information go to https://editorconfig.org/.

## Package Management
The preferred package manager for this starter kit is npm. Npm is currently the most popular choice and has a very large selection of packages to choose from. It also comes with it's own default package security scanner.

Settings for npm are found in package.json.

You will need to download nodejs onto your local machine which comes bundled with npm.

For more information go to https://www.npmjs.com/.

## Development Web Server
The development web server of choice is Express. There is an Express server script found in the buildScripts folder called [srcServer.js](./buildScripts/srcServer.js).

For more information go to https://expressjs.com/.

## Automation
This starter kit runs automation scripts found in the [package.json](./package.json) file at the root. There are multiple scripts that can be run including an eslint script, a localtunnel script which allows you to share your local dev environment via a URL, and most importantly the start scripmt which includes binding, linting, etc.

Running the start script is as easy as running **npm start** in your console.

For more information go to https://docs.npmjs.com/cli/run-script.

## Transpiling
The transpiler of choice for this starter kit is Babel. This will allow developers using this kit to use the latest and greatest JavaScript features but keep compatability everywhere ES 5 is supported.

For more information go to https://babeljs.io/docs/en/.

## Bundling
This starter kit uses webpack as its bundler. Webpack can bundle more than just JavaScript files and allows you to import css, images, etc.

The [webpack config](./webpack.config.dev.js) is found at the root. The config has settings like including an inline source map to be able to debug the original code from the original file and loaders for js and css.

For more information go to https://webpack.js.org/concepts/.

## Linting
For linting this kit uses eslint. The [eslint config](./eslintrc.json) uses the eslint recommended presets which can be tweaked via the rules section. This kit is set up to run lint manually via the lint script in the package.json file and via the npm start script using eslint-watch.

If you are using an eslint plug-in through your editor it will most likely cause issues and should be disabled.

For more information go to https://eslint.org/.

## Testing
This kit is set up with the following testing set up

* Framework
  * [Mocha](https://mochajs.org/)
* Assertion Library
  * [Chai](https://www.chaijs.com/)
* Helper Library
  * [JSDOM](https://github.com/jsdom/jsdom)
* Where are tests run?
  * [Node]()
* Where are the tests?
  * Alongside the js file it is testing
* When are tests run?
  * On save

## Continuous Integration
This kit is set up to use Travis CI for continuous integration.

For more information go to https://travis-ci.org/

