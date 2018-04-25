# linter-farch CLI 👁

#### CLI helper to control filenames of a project 👁

[![Travis CI Build Status](https://travis-ci.org/PaulRosset/linter-farch-cli.svg?branch=master)](https://travis-ci.org/PaulRosset/linter-farch-cli)
[![npm version](https://badge.fury.io/js/linter-farch-cli.svg)](https://badge.fury.io/js/linter-farch-cli)

![](demo.gif)

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

Inside the `farch` property, insert the directory that you want to test.  
Pass as `key`, the path from the root directory to the target directory, then in value pass `regex` to match.  
**Then, you are all set!**

### Execution

At the root of your project:

```sh
farch
```

## API for this module

[linter-farch API](https://github.com/PaulRosset/linter-farch)

## License

MIT Paul Rosset
