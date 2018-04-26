# linter-farch CLI 👁

#### CLI helper to control filenames of a project

[![npm version](https://badge.fury.io/js/linter-farch-cli.svg)](https://badge.fury.io/js/linter-farch-cli)

<div style="width: 100%;">
  <img src="media/demo1" alt="demo-farch-1" style="width: 49%"/>
  <img src="media/demo2" alt="demo-farch-2" style="width: 50%"/>
</div>

## Motivation

More and more frameworks that have been created recently give the possibility to the user to write content in markdown, like [Gatsby](https://github.com/gatsbyjs/gatsby) or [Docusaurus](https://github.com/facebook/docusaurus) and sometimes if you collaborate with multiples persons on this markdown files, keeping an clean file name is more important than ever. That's why I created this tiny linter to force people to respect a filename architecture in order the keep everything clean and understanble.

## Install

```sh
yarn add --dev linter-farch-cli
```

or

```sh
npm i --save-dev linter-farch-cli
```

## Usage

Once installed, a small and quick configuration is needed in the `package.json` file.  
The `package.json` file is used here to avoid creating another file with a purpose of configuration.

### Configuration:

In the `package.json` file:

```json
{
  "farch": {
    "src": "([a-z]*-[0-9]{4})[.]*[a-z]*",
    "src/utilities": "[a-z]*"
  }
}
```

Inside the `farch` property, insert the directory that you want to test:  
Pass as `key`, the path from the root directory to the target directory, then in value pass `regex` to match.

**Then, you are all set!**

### Execution

At the root of your project:

```sh
npx farch
```

or

Insert it in your `package.json` file:

```json
{
  "scripts": {
    "test": "farch"
  }
}
```

## Todo

* [] Extend the config support, let the possibility to use another file than `package.json`, for the non-js project.
* [] A lot of things can be added on top of it...

## API for this module

[linter-farch API](https://github.com/PaulRosset/linter-farch)

## License

MIT Paul Rosset
