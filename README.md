# grunt-flow ![Build Status](https://secure.travis-ci.org/larsonjj/grunt-flow.png?branch=master)

> Validates JavaScript with Facebook's [Flow](https://github.com/facebook/flow) Library

## Getting Started
This plugin requires Grunt.

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-flow --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-flow');
```

## The "flow" task

### Overview
In your project's Gruntfile, add a section named `flow` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  flow: {
    options: {}
  },
  files: {}
})
```

### Options

#### options.style
Type: `String`
Default value: `color`

A string value that is used to determine flow output styling. There are two options to choose from:

1. `color` - This will colorize the output from flow
2. `none` - This will keep the default standard text output from flow without any color.

### Usage

#### Config

[Flow](https://github.com/facebook/flow) requires that you have a `.flowconfig` file in the root of you project folder. Below is an example of what your `.flowconfig` file should look like:

```bash
# .flowconfig
[include]

[ignore]
.*/node_modules/flow-bin
```

You can look up more information on the `.flowconfig` file on the flow [website](http://flowtype.org/docs/advanced-configuration.html#_)

#### Task

Within your Gruntfile.js, add the following code to enable colorized output for flow.

```js
grunt.initConfig({
  flow: {
    options: {
        style: 'color'
    },
    files: {}  // Flow doesn't use this, but it is needed for Grunt to run properly
  }
})
```



## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History

<strong>v1.0.0</strong> - Updated to latest version of flow (v0.14.0)

<strong>v0.0.3</strong> - Fixed colorized output

<strong>v0.0.2</strong> - Added `style` option to enable colorized output

<strong>v0.0.1</strong> - Initial release

## License
Copyright (c) 2015 Jake Larson. Licensed under the MIT license.
