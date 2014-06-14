oust [![Build Status](https://travis-ci.org/addyosmani/oust.svg?branch=master)](https://travis-ci.org/addyosmani/oust)
====

> Extract a list of stylesheets, scripts or HTML imports from HTML

### Install

```sh
npm install oust --save-dev
```

### Usage

First include:

```js
var oust = require('oust');
```

Resource links can then be extracted from either files:

#### Extract stylesheets references `<link rel="stylesheet">`

```js
var hrefs = oust(htmlString);
```

#### Extract script references `<script src>`

```js
var srcs = oust(htmlString, 'script');
```

#### Extract HTML imports `<link rel="import">`

```js
var hrefs = oust(htmlString, 'import');
```

### API

#### Options

Attribute       | Default   | Description
---             | ---       | ---
`src`           | ``        | a valid HTML string to parse for references
`type`      | `link[rel="stylesheet"]`        | one of `link`, `script`, `import`

### License

Released under an Apache 2 license. © Google 2014.