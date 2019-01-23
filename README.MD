# Java Script Starter Kit

This is a starter kit for any JavaScript development. It was developed using the Pluralsight course [Building a JavaScript Development Environment](https://www.pluralsight.com/courses/javascript-development-environment).

## Get Started

1. **Install [Node 6 or newer](https://nodejs.org)**. Need to run multiple versions of Node? Use [nvm](https://github.com/creationix/nvm) or [nvm-windows](https://github.com/coreybutler/nvm-windows)
2. **Clone this repository.** - `git clone https://github.com/coryhouse/javascript-development-environment.git` or [download the zip](https://github.com/coryhouse/javascript-development-environment/archive/master.zip)
3. **Make sure you're in the directory you just created.** - `cd javascript-development-environment`
4. **Install Node Packages.** - `npm install`
5. **Run the app.** - `npm start -s`
   This will run the automated build process, start up a webserver, and open the application in your default browser. When doing development with this kit, this command will continue watching files all your files. Every time you hit save the code is rebuilt, linting runs, and tests run automatically. Note: The -s flag is optional. It enables silent mode which suppresses unnecessary messages during the build.
6. Having issues? See below.

## Having Issues? Try these things first:

1. Run `npm install` - If you forget to do this, you'll see this: `babel-node: command not found`.
2. Try running the latest version of Node.
3. Make sure files with names that begin with a dot (.babelrc, .editorconfig, .eslintrc) are copied to the project directory root. This is easy to overlook if you copy this repository manually.
4. Don't run the project from a symbolic link. It will cause issues with file watches.
5. Having linting issues? Delete any .eslintrc that you're storing in your user directory. Also, disable any ESLint plugin / custom rules that you've enabled within your editor. These will conflict with the ESLint rules defined in the course.
6. Seeing `Error: listen EADDRINUSE :::3000`? That means port 3000 is already in use on your machine. You probably have another instance of this project running on your machine in a different window. So find that window and kill the other instance using Ctrl+C.
7. Nothing above work? Delete your node_modules folder and re-run npm install.

### Development Dependencies

| **Dependency**              | **Use**                                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------------------- |
| babel-cli                   | Babel Command line interface                                                                              |
| babel-core                  | Babel Core for transpiling the new JavaScript to old                                                      |
| babel-loader                | Adds Babel support to Webpack                                                                             |
| babel-preset-latest         | Babel preset for running all the latest standardized JavaScript features                                  |
| babel-register              | Register Babel to transpile our Mocha tests                                                               |
| chai                        | Assertion library                                                                                         |
| chalk                       | Colored command line output                                                                               |
| cheerio                     | Supports querying DOM with jQuery like syntax - Useful in testing and build process for HTML manipulation |
| compression                 | gzip http output                                                                                          |
| cross-env                   | Cross-environment friendly way to handle environment variables                                            |
| css-loader                  | Add CSS support to Webpack                                                                                |
| eslint                      | Lints JavaScript                                                                                          |
| eslint-plugin-import        | Advanced linting of ES6 imports                                                                           |
| eslint-watch                | Add watch functionality to ESLint                                                                         |
| express                     | Serves development and production builds                                                                  |
| extract-text-webpack-plugin | Extracts CSS into separate file for production build                                                      |
| html-webpack-plugin         | Generate HTML file programatically via Webpack                                                            |
| jsdom                       | In-memory DOM for testing                                                                                 |
| json-schema-faker           | Declare a JSON schema for generating fake data                                                            |
| json-server                 | Serve a JSON API locally                                                                                  |
| localtunnel                 | Create a tunnel to your local machine                                                                     |
| mocha                       | JavaScript testing library                                                                                |
| nock                        | Mock HTTP requests via Node                                                                               |
| npm-run-all                 | Display results of multiple commands on single command line                                               |
| numeral                     | Library for working with numbers                                                                          |
| open                        | Open app in default browser                                                                               |
| rimraf                      | Delete files                                                                                              |
| style-loader                | Add Style support to Webpack                                                                              |
| webpack                     | Bundler with plugin system and integrated development server                                              |
| webpack-dev-middleware      | Adds middleware support to webpack                                                                        |
| webpack-hot-middleware      | Adds hot reloading to webpack                                                                             |
| webpack-md5-hash            | Used to hash files generated by Webpack using MD5 so that their names change when the content changes     |


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
This kit offers two options for continuous integration [Travis CI](https://travis-ci.org/) and [Appveyor](https://www.appveyor.com/).

## HTTP Calls
This kit is currently set up to use Fetch to make HTTP calls to apis. This is encapsulated in the centralized API call layer [userApi.js](./src/api/userApi.js);

For more information about Fetch go to https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API.

## Api Mocking
This kit uses the following tools to mock an API layer:

1. Declare our schema:
  - [JSON Schema Faker](https://json-schema-faker.js.org/)

2. Generate Randomn Data
  - [faker.js](https://www.npmjs.com/package/faker)
  - [chance.js](https://chancejs.com/)
  - [randexp](https://www.npmjs.com/package/randexp)

3. Serve Data via API
  - [JSON Server](https://github.com/typicode/json-server)

## Production Build
Below are the specific settings for the default production build. Most of these are acheived through the separate [webpack.config.prod.js](./webpack.config.prod.js) configuration file. For more information about Webpack go to https://webpack.js.org/concepts/

All production build files are output to a separate folder named "dist". This folder is checked into source control but any file in the folder are ignored.

The production build script [buld.js](./buildScripts/build.js) calls webpack config and adds some error handling and status output to the console. This also gives the developer the ability to build and run the production version of the app locally. The local [express server](./buildScripts/srcServer.js) uses gzip compression to serve any files locally. This gives a good indication to the size of any files when they are served in production

The build script is automated through the "build" script in the [package.json](./package.json) file.

### Minification
This kit uses a Webpack plug-in called Uglify JS. This minifies all js files. The Dedupe plug-in is also used to eliminate any duplicate packages.

### Sourcemaps
The source maps have been set to 'source map' for the devtool setting. This creates a longer build but enhances the debugging experience for production. The source maps are only downloaded if you open the developer tools in the browser.

### Minified HTML and Dynamic Script Tags
The HTML for this starter kit is minified and the script tags are dynamically inhected using the HTML-Webpack plug-in.

### Cache Busting
Cache busting is acheived by hashing all files. This way the files will only be served to the client when they have actually changed. This is achieved by using the Webpack Md5 Hash plugin and inserting the chunk hash into the filename under output in the config file like this '\[name\].\[chunk\].js'

### Bundle Splitting
The javascript for this kit are bundled into application javascript and third party or vendor javascript files. That way if the application javascript source changes the client doesn't have to download all js files.

Bundle splitting is achieved through Webpack plug-in Commons Chunk. Each javascript file has an entry in the 'entry' section of the config file. The entry name must be the same as tne name in the plug-in declaration. The filename in the output section must also be dynamic using '\[name\].js'.

### Error Logging
This starter project uses TraackJS by dynamically inserting the TrackJS script tag into the Head tag only if the environment is production. It also utilizes an environment variable found in the Webpack config file which contains the specific TrackJS token. The dynamic html is acheieved using Embedded JS for more information on Embedded JS go to https://ejs.co/.

For more information on TrackJS go to https://trackjs.com.
