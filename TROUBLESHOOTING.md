# TROUBLESHOOTING

## Parcel

1. Feature: Parcel build for static sites, meaning pure frontend. Javascript and HTML only.
Static files can be loaded from browser like a saved website. 

// TODO package.json/folder structure/build parameters

2. Problem: Parcel build, problem with include src calculated paths
By default the resolved paths to css/js includes in HTML are set with absolute path
example: 
```
<script src="index.18dbc454.js" defer=""></script>
```
BUT to load the src not from a server but viewing it like a static saved webpage. Then the solution is to allow for simpler path resolve uisng relative paths.
```
want to resolve to this:
<script src="./index.18dbc454.js" defer=""></script>
```

2. Solution: 
using the `--public-url` flag

example:
```
parcel build src/js/main.js --public-url ./
```

source: https://parceljs.org/features/targets/#publicurl