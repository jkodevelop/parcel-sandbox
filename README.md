# PARCEL quick guide [2025]

This project is a quick quide to use PARCEL for basic configurations that is useful for a project.

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



#### source

https://parceljs.org/
