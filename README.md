# PARCEL quick guide [2025]

This project is a quick quide to use PARCEL for basic configurations that is useful for a project.
Parcel can start from html file and know the starting points of css and js file by default.

## 1. install Parcel and usages

Install the package
```
$ npm install -D parcel
```

Running Parcel, this will run a local server and build the files. Default output `./dist`
```
$ npx parcel src/index.html
```

To just build the project, note: command needs the source starting point
```
$ npx parcel build src/index.html
```

**Important note:** In `package.json` remove default *"main": "index.js",* to enable the simplest build only with .html file.

## 1b. package.json configuration options

Parcel uses package.json for some more basic information.
The source can be place in package.json instead of the cli

In package.json
```
"source": "src/index.html",
"scripts": {
  "start": "parcel",
  "build": "parcel build"
}
```

## 1c. notes on Parcel V2 build features

1. Currently Parcel v2 does not have a library or feature to cleanup the `./dist` folder after. The folder needs to be cleared out manually.

2. some CLI options
```
"start": "parcel --port=1234 --open",
"build": "parcel build --public-url ./ --dist-dir dist"
```

## 2. SASS support

Parcel V2 has sass support built-in, it will auto install sass the moment sass files are included.

## 3. posthtml, templating

To support html templating. using this `<include src="./tpl/header-tpl.html"></include>` in the index.html for easier templating.

1. install the package
```
npm install posthtml-include --save-dev
```

2. add the file `.posthtmlrc`, point to `./src` folder
```
{
  "plugins": {
    "posthtml-include": {
      "root": "./src"
    }
  }
}
```

3. using this feature in `index.html`
```
<include src="src/tpl/tplA.html"></include>
```



#### source

https://parceljs.org/
