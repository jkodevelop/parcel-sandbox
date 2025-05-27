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



#### source

https://parceljs.org/
