# FireDocs

Firebase JSDocs Template.

All credit goes to [nijikokun([https://github.com/nijikokun/minami).

![FireDocs Screenshot](http://puu.sh/gOyNe/66c3adcb97.png)

## Uses

- [the Taffy Database library](http://taffydb.com/)
- [Underscore Template library](http://documentcloud.github.com/underscore/#template)
- [Montserrat](http://www.google.com/fonts/specimen/Monsterrat) & Helvetica Neue

## Install

```bash
$ npm install --save-dev FireDocs
```

## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/FireDocs
```

### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc --configure .jsdoc.json --verbose"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/FireDocs"
}
```

### Example JSDoc Config

```json
{
    "tags": {
        "allowUnknownTags": true,
        "dictionaries": ["jsdoc"]
    },
    "source": {
        "include": ["lib", "package.json", "README.md"],
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "templates": {
        "cleverLinks": false,
        "monospaceLinks": true,
        "useLongnameInNav": false
    },
    "opts": {
        "destination": "./docs/",
        "encoding": "utf8",
        "private": true,
        "recurse": true,
        "template": "./node_modules/FireDocs"
    }
}
```

Specifying a number for useLongnameInNav it will be the max number of path elements to show in nav (starting from Class).

## License

Licensed under the Apache2 license.
