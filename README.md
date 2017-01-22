Pug support for SourceJS
===============

[![Greenkeeper badge](https://badges.greenkeeper.io/JohannesFischer/sourcejs-pug.svg)](https://greenkeeper.io/)

[SourceJS](http://sourcejs.com) middleware to support [Pug](https://pugjs.org/) markup language (`*.pug`) instead of native `*.src`.

Works with SourceJS v.0.5.6+.

## Install

To install, run npm in `sourcejs/user` folder:

```
npm install sourcejs-pug --save
```

Then add `index.pug` to the list of spec files in your user options file.

```javascript
// Page rendering configuration (redefinable from context options)
rendering: {
  // Define priority of spec file source
  specFiles: [
    'index.src',
    'index.src.html',
    'index.jade', // https://www.npmjs.com/package/sourcejs-jade
    'index.pug', // https://www.npmjs.com/package/sourcejs-pug
    'index.jsx', // https://www.npmjs.com/package/sourcejs-react
    'index.md',
    'readme.md',
    'README.md',
    'index.html'
  ],
},
```

Then restart your SourceJS application, middleware will be loaded automatically.

## Usage

After installing middleware, instead of `index.src` pages, you can `index.pug` files with Pug markup.

index.pug

```
h1 Pug - node template engine

#container.col
  p.
    Pug is a terse and simple
    templating language with a
    strong focus on performance
    and powerful features.
```