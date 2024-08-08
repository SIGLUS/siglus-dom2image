# siglus-dom2image
- dom-to-image only for bower

Main code is from [tsayen/dom-to-image](https://github.com/tsayen/dom-to-image/blob/master/src/dom-to-image.js)

No function change, only make it compatible with bower

## After Update This Repo

After update and commit & push the code, the following steps are supposed to be done:

1. update the version number in `bower.json` and `bower.json`

```
{
  "version": "1.0.5",  // update this number
  ...
}
```

2. add tag and push the tag for this repo

```
git tag -a 1.0.5 // add tag 
git tag -a 1.0.5 -m "Versoin 1.0.5"  // add tag with comments
```

3. update version in `package-yarn.json` at the repo of [siglus-ui](https://github.com/SIGLUS/siglus-ui)

go to [SIGLUS/siglus-ui](https://github.com/SIGLUS/siglus-ui), update `package-yarn.json`


```
{
  "dependencies": {
    "@bower_components/perfect-scrollbar": "noraesae/perfect-scrollbar-bower#0.6.12",
    "@bower_components/bower-iframe-resizer": "davidjbradshaw/iframe-resizer#4.3.2",
    "@bower_components/dom-to-image":"SIGLUS/siglus-dom2image.git#^1.0.5",  // update this version number to latest tag version
    ...
  },
  ...
}
```

4. rebuild the `siglus-ui`

```
grunt clean yarn build --serve --openlmisServerURL=https://dev.siglus.us  --noTest --noDocs --noStyleguide --force
```
