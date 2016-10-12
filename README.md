#A Solid Development Environment Setup


**Gagan Goswami, Architect**  
*June 29, 2016*
[GITHUB](https://github.com/GaganGoswami/DevEnvSetup.git)

 Introduction
=====
Before writing code we should setup a solid development environment to start a project. Following are the goals for a solid development environment.

Goals:
---
	- Automated Testing
	- Linting
	- Minification
	- Bundling
	- ES6 transpiration

	Our target is to perform all of these tasks using one single command.

Tech Overview
----
I am going to cover following technologies in this blog:

* Babel  6.
* Babel-Polyfill
* web pack module bundler   1.13
* mocha  - testing   
* eslint - Code linting
* redux - 3.5.2
* react/router 2.4.0
* nodeJS

Hot Reloading
---

babel-preset-react-hmre

Warning:
	Experimental
	Doesn't reload functional components
	doesn't reload container functions like mapStore to Props
	other options exist

Production Dependencies
---
|Dependency|Use|
|----------|------|
|babel-polyfill|Polyfill for Babel features that cannot be transpiled|
|bootstrap|CSS Framework|
|react|React library|
|react-dom|React library for DOM rendering|
|react-redux|Redux library for connecting React components to Redux|
|react-router|React library for routing|
|react-router-redux|Keep React Router in sync with Redux application state|
|redux|Library for unidirectional data flows|
|redux-thunk|Async redux library|
|toastr|Display messages to the user|
|jquery|Only used to support toastr|

###Development Dependencies
| **Dependency** | **Use** |
|----------|-------|
|babel-cli|Babel Command line interface |
|babel-core|Babel Core for transpiling the new JavaScript to old |
|babel-loader|Adds Babel support to Webpack |
|babel-plugin-react-display-name| Add displayName to React.createClass calls |
|babel-preset-es2015|Babel preset for ES2015|
|babel-preset-react| Add JSX support to Babel |
|babel-preset-react-hmre|Hot reloading preset for Babel|
|babel-register|Register Babel to transpile our Mocha tests|
|cheerio|Supports querying DOM with jQuery like syntax - Useful in testing and build process for HTML manipulation|
|colors|Adds color support to terminal |
|compression|Add gzip support to Express|
|cross-env|Cross-environment friendly way to handle environment variables|
|css-loader|Add CSS support to Webpack|
|enzyme|Simplified JavaScript Testing utilities for React|
|eslint|Lints JavaScript |
|eslint-plugin-import|Advanced linting of ES6 imports|
|eslint-plugin-react|Adds additional React-related rules to ESLint|
|eslint-watch|Add watch functionality to ESLint |
|eventsource-polyfill|Polyfill to support hot reloading in IE|
|expect|Assertion library for use with Mocha|
|express|Serves development and production builds|
|extract-text-webpack-plugin| Extracts CSS into separate file for production build |
|file-loader| Adds file loading support to Webpack |
|jsdom|In-memory DOM for testing|
|mocha| JavaScript testing library |
|nock| Mock HTTP requests for testing |
|npm-run-all| Display results of multiple commands on single command line |
|open|Open app in default browser|
|react-addons-test-utils| Adds React TestUtils |
|redux-immutable-state-invariant|Warn when Redux state is mutated|
|redux-mock-store|Mock Redux store for testing|
|rimraf|Delete files |
|style-loader| Add Style support to Webpack |
|url-loader| Add url loading support to Webpack |
|webpack| Bundler with plugin system and integrated development server |
|webpack-dev-middleware| Adds middleware support to webpack |
|webpack-hot-middleware| Adds hot reloading to webpack |

```javascript
{
  "name": "DevEnvSetup",
  "version": "1.0.0",
  "description": "Development Environment setup for Javascript Application Development",
  "author": "Gagan Goswami",
  "license": "MIT",
  "dependencies": {
    "babel-polyfill": "6.8.0",
    "bootstrap": "3.3.6",
    "jquery": "2.2.3",
    "react": "15.0.2",
    "react-dom": "15.0.2",
    "react-redux": "4.4.5",
    "react-router": "2.4.0",
    "react-router-redux": "4.0.4",
    "redux": "3.5.2",
    "redux-thunk": "2.0.1",
    "toastr": "2.1.2"
  },


  "devDependencies": {
    "babel-cli": "6.8.0",
    "babel-core": "6.8.0",
    "babel-loader": "6.2.4",
    "babel-plugin-react-display-name": "2.0.0",
    "babel-preset-es2015": "6.6.0",
    "babel-preset-react": "6.5.0",
    "babel-preset-react-hmre": "1.1.1",
    "babel-register": "6.8.0",
    "colors": "1.1.2",
    "compression": "1.6.1",
    "cross-env": "1.0.7",
    "css-loader": "0.23.1",
    "enzyme": "2.2.0",
    "eslint": "2.9.0",
    "eslint-plugin-import": "1.6.1",
    "eslint-plugin-react": "5.0.1",
    "eslint-watch": "2.1.11",
    "eventsource-polyfill": "0.9.6",
    "expect": "1.19.0",
    "express": "4.13.4",
    "extract-text-webpack-plugin": "1.0.1",
    "file-loader": "0.8.5",
    "jsdom": "8.5.0",
    "mocha": "2.4.5",
    "nock": "8.0.0",
    "npm-run-all": "1.8.0",
    "open": "0.0.5",
    "react-addons-test-utils": "15.0.2",
    "redux-immutable-state-invariant": "1.2.3",
    "redux-mock-store": "1.0.2",
    "rimraf": "2.5.2",
    "style-loader": "0.13.1",
    "url-loader": "0.5.7",
    "webpack": "1.13.0",
    "webpack-dev-middleware": "1.6.1",
    "webpack-hot-middleware": "2.10.0"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/GaganGoswami/DevEnvSetup.git"
  }
}
```


Code Editors:
---

[Sub Lime Text](https://www.sublimetext.com)
---

	Sublime Text is a sophisticated text editor for code, markup and prose.
You'll love the slick user interface, extraordinary features and amazing performance.

####Goto Anything
Use Goto Anything to open files with only a few keystrokes, and instantly jump to symbols, lines or words.
Triggered with ⌘P, it is possible to:

* Type part of a file name to open it.
* Type @ to jump to symbols, # to search within the file, and : to go to a line number.

####Multiple Selections

Make ten changes at the same time, not one change ten times. Multiple selections allow you to interactively change many lines at once, rename variables with ease, and manipulate files faster than ever.

Try pressing ⇧⌘L to split the selection into lines and ⌘D to select the next occurrence of the selected word. To make multiple selections with the mouse, take a look at the Column Selection documentation.

####Command Palette

The Command Palette holds infrequently used functionality, like sorting, changing the syntax and changing the indentation settings. With just a few keystrokes, you can search for what you want, without ever having to navigate through the menus or remember obscure key bindings.

Show the Command Palette with ⌘⇧P.

####Distraction Free Mode

When you need to focus, Distraction Free Mode is there to help you out. Distraction Free Mode is full screen, chrome free editing, with nothing but your text in the center of the screen.

You can enter Distraction Free Mode using the View/Enter Distraction Free Mode menu.


####Split Editing

Get the most out of your wide screen monitor with split editing support. Edit files side by side, or edit two locations in the one file. You can edit with as many rows and columns as you wish.

Take a look at the View/Layout menu for split editing options. To open multiple views into the one file, use the File/New View into File menu item.


####Instant Project Switch

Projects in Sublime Text capture the full contents of the workspace, including modified and unsaved files. You can switch between projects in a manner similar to Goto Anything, and the switch is instant, with no save prompts - all your modifications will be restored next time the project is opened.

####Plugin API

Sublime Text has a powerful, Python based plugin API. Along with the API, it comes with a built in Python console to interactively experiment in real time.

####Cross Platform

Sublime Text is available for OS X, Windows and Linux. One license is all you need to use Sublime Text on every computer you own, no matter what operating system it uses.

[Atom](https://atom.io):
---

Atom is a text editor that's modern, approachable, yet hackable to the core—a tool you can customize to do anything but also use productively without ever touching a config file.

#####Full-featured, right out of the box
####Cross-platform editing
Atom works across operating systems. You can use it on OS X, Windows, or Linux.


####Built-in package manager
Search for and install new packages or start creating your own—all from within Atom.


####Smart autocompletion
Atom helps you write code faster with a smart, flexible autocomplete.

####File system browser
Easily browse and open a single file, a whole project, or multiple projects in one window.


####Multiple panes
Split your Atom interface into multiple panes to compare and edit code across files.


####Find and replace
Find, preview, and replace text as you type in a file or across all your projects.

####Note:

    Java developers can also use eclipse but these editors are very light weight and provide lots of other functionality. These editors are plug-in/package based.  Those we can download as per requirements. 										

NPM Scripts:
----

* Easy to learn
* Simple
* No Extra layer of abstraction
* No dependency on separate plugins
* Simple debugging than gulp
* Better DocUmentation

		Read More : bit.ly/npmvsgulp

WebPack:
---
// description and basic setup of webpack

```javascript
import webpack from 'webpack';
import path from 'path';

export default {
  debug: true,  // For debugging
  devtool: 'cheap-module-eval-source-map',
  noInfo: false, // for bundling
  entry: [
    'eventsource-polyfill', // necessary for hot reloading with IE
    'webpack-hot-middleware/client?reload=true', //note that it reloads the page if hot module reloading fails.
    './src/index'
  ],
  target: 'web',
  output: {
    path: __dirname + '/dist', // Note: Physical files are only output by the production build task `npm run build`.
    publicPath: '/',
    filename: 'bundle.js'
  },
  devServer: {
    contentBase: './src'
  },
  plugins: [
    new webpack.HotModuleReplacementPlugin(),
    new webpack.NoErrorsPlugin()
  ],
  module: {
    loaders: [
      {test: /\.js$/, include: path.join(__dirname, 'src'), loaders: ['babel']},
      {test: /(\.css)$/, loaders: ['style', 'css']},
      {test: /\.eot(\?v=\d+\.\d+\.\d+)?$/, loader: 'file'},
      {test: /\.(woff|woff2)$/, loader: 'url?prefix=font/&limit=5000'},
      {test: /\.ttf(\?v=\d+\.\d+\.\d+)?$/, loader: 'url?limit=10000&mimetype=application/octet-stream'},
      {test: /\.svg(\?v=\d+\.\d+\.\d+)?$/, loader: 'url?limit=10000&mimetype=image/svg+xml'}
    ]
  }
};

```

package.json:
---

```javascript
{
  "name": "DevEnvSetup",
  "version": "1.0.0",
  "description": "Development Environment setup for Javascript Application Development",
  "author": "Gagan Goswami",
  "license": "MIT",
  "scripts": {
    "prestart": "babel-node tools/startMessage.js",
    "start": "npm-run-all --parallel test:watch open:src lint:watch",
    "open:src": "babel-node tools/server.js",
    "lint": "node_modules/.bin/esw webpack.config.* src tools",
    "lint:watch": "npm run lint -- --watch",
    "test": "mocha --reporter progress tools/testSetup.js \"src/**/*.test.js\"",
    "test:watch": "npm run test -- --watch"
  },
  "dependencies": {
    "babel-polyfill": "6.8.0",
    "bootstrap": "3.3.6",
    "jquery": "2.2.3",
    "react": "15.0.2",
    "react-dom": "15.0.2",
    "react-redux": "4.4.5",
    "react-router": "2.4.0",
    "react-router-redux": "4.0.4",
    "redux": "3.5.2",
    "redux-thunk": "2.0.1",
    "toastr": "2.1.2"
  },
  "devDependencies": {
    "babel-cli": "6.8.0",
    "babel-core": "6.8.0",
    "babel-loader": "6.2.4",
    "babel-plugin-react-display-name": "2.0.0",
    "babel-preset-es2015": "6.6.0",
    "babel-preset-react": "6.5.0",
    "babel-preset-react-hmre": "1.1.1",
    "babel-register": "6.8.0",
    "colors": "1.1.2",
    "compression": "1.6.1",
    "cross-env": "1.0.7",
    "css-loader": "0.23.1",
    "enzyme": "2.2.0",
    "eslint": "2.9.0",
    "eslint-plugin-import": "1.6.1",
    "eslint-plugin-react": "5.0.1",
    "eslint-watch": "2.1.11",
    "eventsource-polyfill": "0.9.6",
    "expect": "1.19.0",
    "express": "4.13.4",
    "extract-text-webpack-plugin": "1.0.1",
    "file-loader": "0.8.5",
    "jsdom": "8.5.0",
    "mocha": "2.4.5",
    "nock": "8.0.0",
    "npm-run-all": "1.8.0",
    "open": "0.0.5",
    "react-addons-test-utils": "15.0.2",
    "redux-immutable-state-invariant": "1.2.3",
    "redux-mock-store": "1.0.2",
    "rimraf": "2.5.2",
    "style-loader": "0.13.1",
    "url-loader": "0.5.7",
    "webpack": "1.13.0",
    "webpack-dev-middleware": "1.6.1",
    "webpack-hot-middleware": "2.10.0"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/GaganGoswami/DevEnvSetup.git"
  }
}

```
Editorconfig
---

Create .editorconfig file if team uses diffrent editors for development.

```javascript
# editorconfig.org
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.md]
trim_trailing_whitespace = false

```


Babelrc
---

Create .babelrc file for Babel preset.
This configuration is also required for Hot reloading in development environment.

```javascript
{
  "presets": ["react", "es2015"],
  "env": {
    "development": {
      "presets": ["react-hmre"]
    }
  }
}
```

.eslintrc
---

Create this file in root directory for Javascript Lint configurations.

```javascript
{
  "extends": [
    "eslint:recommended",
    "plugin:import/errors",
    "plugin:import/warnings"
  ],
  "plugins": [
    "react"
  ],
  "parserOptions": {
    "ecmaVersion": 6,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true,
    "jquery": true,
    "mocha": true
  },
  "rules": {
    "quotes": 0,
    "no-console": 1,
    "no-debugger": 1,
    "no-var": 1,
    "semi": [1, "always"],
    "no-trailing-spaces": 0,
    "eol-last": 0,
    "no-unused-vars": 0,
    "no-underscore-dangle": 0,
    "no-alert": 0,
    "no-lone-blocks": 0,
    "jsx-quotes": 1,
    "react/display-name": [ 1, {"ignoreTranspilerName": false }],
    "react/forbid-prop-types": [1, {"forbid": ["any"]}],
    "react/jsx-boolean-value": 1,
    "react/jsx-closing-bracket-location": 0,
    "react/jsx-curly-spacing": 1,
    "react/jsx-indent-props": 0,
    "react/jsx-key": 1,
    "react/jsx-max-props-per-line": 0,
    "react/jsx-no-bind": 1,
    "react/jsx-no-duplicate-props": 1,
    "react/jsx-no-literals": 0,
    "react/jsx-no-undef": 1,
    "react/jsx-pascal-case": 1,
    "react/jsx-sort-prop-types": 0,
    "react/jsx-sort-props": 0,
    "react/jsx-uses-react": 1,
    "react/jsx-uses-vars": 1,
    "react/no-danger": 1,
    "react/no-did-mount-set-state": 1,
    "react/no-did-update-set-state": 1,
    "react/no-direct-mutation-state": 1,
    "react/no-multi-comp": 1,
    "react/no-set-state": 0,
    "react/no-unknown-property": 1,
    "react/prefer-es6-class": 1,
    "react/prop-types": 1,
    "react/react-in-jsx-scope": 1,
    "react/require-extension": 1,
    "react/self-closing-comp": 1,
    "react/sort-comp": 1,
    "react/wrap-multilines": 1
  }
}

```

Setup Express server:
---

Create server.js file and configure express server so that it can serve files in the development environment

```javascript
import express from 'express';
import webpack from 'webpack';
import path from 'path';
import config from '../webpack.config.dev';
import open from 'open';

/* eslint-disable no-console */

const port = 3000;
const app = express();
const compiler = webpack(config);

app.use(require('webpack-dev-middleware')(compiler, {
  noInfo: true,
  publicPath: config.output.publicPath
}));

app.use(require('webpack-hot-middleware')(compiler));

app.get('*', function(req, res) {
  res.sendFile(path.join( __dirname, '../src/index.html'));
});

app.listen(port, function(err) {
  if (err) {
    console.log(err);
  } else {
    open(`http://localhost:${port}`);
  }
});

```

.gitignore
---

Create this file in case team is using gift repository and like to ignore some development environments files to get repo. For example:  node_modules,  log files, local configuration files.

```javascript
# Logs
logs
*.log

# Runtime data
pids
*.pid
*.seed

# Directory for instrumented libs generated by jscoverage/JSCover
lib-cov

# Coverage directory used by tools like istanbul
coverage

# Grunt intermediate storage (http://gruntjs.com/creating-plugins#storing-task-files)
.grunt

# node-waf configuration
.lock-wscript

# Compiled binary addons (http://nodejs.org/api/addons.html)
build/Release

# Dependency directory
# https://www.npmjs.org/doc/misc/npm-faq.html#should-i-check-my-node_modules-folder-into-git
node_modules

#dist folder
dist

#Webstorm metadata
.idea

# Mac files
.DS_Store

```
Scripts
---

In package.json we can have scripts setup.
Ex: start, restart, poststart

If we execute non start then the all the scripts execute in the order `prestart > start > poststart`

Lint:
---

We can setup lint in the scripts section of the package.json file. Lint will run rule based on .eslintrc file.

```javascript
“lint”: “node_module/.bin/esw webpack.config.* src tools”
```
Using command >`npm run lint`
We can execute above lint script.

Lint:watch:
---

Lint watch is used to  check all listing when a file changed. It will display linting error/warning in console.

```javascript
"lint": "node_modules/.bin/esw webpack.config.* src tools",
 "lint:watch": "npm run lint -- --watch",
```

Running multiple scripts together:
---

we can define in sub tasks and run all task @ start like

```javascript
    "start": "npm-run-all --parallel test:watch open:src lint:watch",
    "open:src": "babel-node tools/server.js",
 ```

And run command >  `npm start –s`  // -s for silent mode

Setup Automated Testing:
---

Create a test setup file under tools directory:

```javascript
    "test": "mocha --reporter progress tools/testSetup.js \"src/**/*.test.js\"",
    "test:watch": "npm run test -- --watch"
```

and

`"start": "npm-run-all --parallel test:watch open:src lint:watch",`

Test Stub:
---

```javascript
import expect from 'expect';

describe('First Test stub',() => {
  it('should pass',() => {
    expect(true).toEqual(true);
  });
});

```


