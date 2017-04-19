# npmdoc-maildev

#### api documentation for  [maildev (v0.14.0)](http://djfarrelly.github.io/MailDev/)  [![npm package](https://img.shields.io/npm/v/npmdoc-maildev.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-maildev) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-maildev.svg)](https://travis-ci.org/npmdoc/node-npmdoc-maildev)

#### SMTP Server and Web Interface for reading and testing emails during development

[![NPM](https://nodei.co/npm/maildev.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/maildev)

- [https://npmdoc.github.io/node-npmdoc-maildev/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-maildev/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-maildev/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-maildev/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-maildev/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-maildev/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Farrelly"
    },
    "bin": {
        "maildev": "./bin/maildev"
    },
    "bugs": {
        "url": "https://github.com/djfarrelly/maildev/issues"
    },
    "dependencies": {
        "async": "1.5.1",
        "commander": "2.9.0",
        "express": "4.13.4",
        "mailparser": "0.5.3",
        "open": "0.0.5",
        "simplesmtp": "0.3.35",
        "smtp-connection": "2.3.1",
        "smtp-server": "1.4.0",
        "socket.io": "1.4.5",
        "wildstring": "1.0.8"
    },
    "description": "SMTP Server and Web Interface for reading and testing emails during development",
    "devDependencies": {
        "grunt": "0.4.5",
        "grunt-concurrent": "2.2.1",
        "grunt-contrib-jshint": "1.0.0",
        "grunt-contrib-watch": "1.0.0",
        "grunt-nodemon": "0.4.1",
        "grunt-sass": "1.1.0",
        "http-proxy-middleware": "0.12.0",
        "istanbul": "0.4.4",
        "matchdep": "1.0.1",
        "mocha": "2.2.5",
        "nodemailer": "2.3.0",
        "request": "2.69.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5c0ba72c804a8678f872c4e1a871c849ffa9da22",
        "tarball": "https://registry.npmjs.org/maildev/-/maildev-0.14.0.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "4edecfcf1cd7fe173bbe5c78fb9ead71d2756b8e",
    "homepage": "http://djfarrelly.github.io/MailDev/",
    "keywords": [
        "email",
        "e-mail",
        "mail",
        "mailcatcher"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "djfarrelly"
        }
    ],
    "name": "maildev",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/djfarrelly/maildev.git"
    },
    "scripts": {
        "test": "istanbul cover _mocha"
    },
    "version": "0.14.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
