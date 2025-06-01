# React + PARCEL quick guide [2025]

Parcel is simplist bundler for react. It just supports react out of the box.

## 1. install React packages

Install the package
```
$ npm install --save react react-dom
```


## 2. update package.json

Point source to the starting point
```
"source": "src/index.html",
```


## 3. SASS support

Parcel V2 has sass support built-in, it will auto install sass the moment sass files are included.


## 4. Run it

package.json
```
"scripts": {
  "start": "parcel --port=1234 --open",
  "build": "parcel build --dist-dir dist"
}
```

run
```
$ npm start
```



#### source

https://parceljs.org/