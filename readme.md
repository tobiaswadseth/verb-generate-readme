# verb-readme-generator [![NPM version](https://img.shields.io/npm/v/verb-readme-generator.svg?style=flat)](https://www.npmjs.com/package/verb-readme-generator) [![NPM downloads](https://img.shields.io/npm/dm/verb-readme-generator.svg?style=flat)](https://npmjs.org/package/verb-readme-generator) [![Build Status](https://img.shields.io/travis/verbose/verb-readme-generator.svg?style=flat)](https://travis-ci.org/verbose/verb-readme-generator)

> Generate your project's readme with verb. Requires verb v0.9.0 or higher.

You might also be interested in [generate](https://github.com/generate/generate).

## TOC

- [Install](#install)
- [Usage](#usage)
- [Options](#options)
  * [readme](#readme)
  * [toc](#toc)
    + [layout](#layout)
- [Related projects](#related-projects)
- [Contributing](#contributing)
- [Building docs](#building-docs)
- [Running tests](#running-tests)
- [Author](#author)
- [License](#license)

_(TOC generated by [verb](https://github.com/verbose/verb) using [markdown-toc](https://github.com/jonschlinkert/markdown-toc))_

## Install

Install as a `devDependency` with [npm](https://www.npmjs.com/):

```sh
$ npm install verb-readme-generator --save-dev
```

If you do not already have [verb](https://github.com/verbose/verb) installed globally, you can do that now with the following command:

```sh
$ npm i -g verb
```

## Usage

**Run the generator from the command line**

Once both [verb](https://github.com/verbose/verb) and verb-readme-generator are installed globally, you can run this generator with the following command:

```sh
$ verb verbReadmeGenerator
```

**Automatically run the generator**

In any project where you want this generator to automatically run with the `verb` command instead of `verb readme`, add the following to package.json:

```json
{
  "name": "my-project",
  "version": "0.1.0",
  
  // add a verb config object with the tasks to run
  "verb": {
    "tasks": ["readme"]
  }
}
```

## Options

Configuration options can be passed on the command line, defined on the `verb` object in package.json, or set using the API.

Most of the following examples show how to set configuration values on the `verb` object _via the command line_, but you can also set these manually.

### readme

Customize the location of your readme template.

**CLI**

```sh
$ verb --readme="lib/foo.md"
```

**verb config**

In your project's package.json:

```json
{
  "verb": {
    "readme": "docs/foo.md"
  }
}
```

### toc

Disable or enable the Table of Contents in the built-in layouts:

**CLI**

One-time only (in-memory)

```sh
# enable
$ verb --toc
# disable
$ verb --toc:false
```

Persist the value to package.json:

```sh
# enable
$ verb --config=toc
# disable
$ verb --config=toc:false
```

Results in:

```json
{
  "name": "my-project",
  "verb": {
    "toc": false
  }
}
```

#### layout

Set the layout to use for a project.

```sh
$ verb --config=layout:default
```

**Available layouts**

As with all templates, you can easily override these and/or define your own templates in a `verbfile.js`. Verb does much more than generate readme's!

The following layouts are available:

* `default`: a layout with installation, tests, author, usage, related list, contributing and license sections.
* `global`: same as default, but with global npm installation instructions (verb-readme-generator uses this layout)
* `empty`: noop layout. no content is applied, but all layout-related middleware stages will still run.

Layouts can be defined on a template-by-template basic, and even for includes. If you need more granularity just add a `verbfile.js` with your custom code.

## Related projects

You might also be interested in these projects:

* [verb-collections](https://www.npmjs.com/package/verb-collections): Verb plugin that adds includes, layouts, badges and docs template collections. Can be used with… [more](https://www.npmjs.com/package/verb-collections) | [homepage](https://github.com/verbose/verb-collections)
* [verb-data](https://www.npmjs.com/package/verb-data): Verb plugin that adds commonly needed data to the context for rendering templates. | [homepage](https://github.com/jonschlinkert/verb-data)
* [verb-toc](https://www.npmjs.com/package/verb-toc): Verb generator that adds middleware for creating and injecting a table of contents into a… [more](https://www.npmjs.com/package/verb-toc) | [homepage](https://github.com/verbose/verb-toc)
* [verb](https://www.npmjs.com/package/verb): Documentation generator for GitHub projects. Verb is extremely powerful, easy to use, and is used… [more](https://www.npmjs.com/package/verb) | [homepage](https://github.com/verbose/verb)

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/verbose/verb-readme-generator/issues/new).

## Building docs

Generate readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install verb && npm run docs
```

Or, if [verb](https://github.com/verbose/verb) is installed globally:

```sh
$ verb
```

## Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/verbose/verb-readme-generator/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on April 22, 2016._