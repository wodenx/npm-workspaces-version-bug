## Steps to reproduce

1. Create monorepo with 2 packages (pkg-a and pkg-b).  Both at "1.0.0".  pkg-a depends on pkg-b@^1.0.0
2, npm i at package root. (Initial commit includes package-lock).
3. Bump version of both package a and package b, and update pkg-a dep to pkg-b@^2.0.0
4. npm i at package root.

## Expected Result
Packages install correctly.

## Actual Result
```
npm ERR! code ETARGET
npm ERR! notarget No matching version found for pkg-b@^2.0.0.
npm ERR! notarget In most cases you or one of your dependencies are requesting
npm ERR! notarget a package version that doesn't exist.
```
## Version Info
```
$ npm -v
8.1.2
$ node -v
v16.13.1
```
