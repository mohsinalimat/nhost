# @nhost/hasura-storage-js

## 0.0.12

### Patch Changes

- 8f7643a: Change target ES module build target to es2019
  Some systems based on older versions of Webpack or Babel don't support the current esbuild configuration e.g, [this issue](https://github.com/nhost/nhost/issues/275).

## 0.0.11

### Patch Changes

- 35f0ee7: Rename `storage.getUrl` to `storage.getPublicUrl`
  It aims to make a clear distinction between `storage.getPublicUrl` and `storage.getPresginedUrl`
  `storage.getUrl` is now deprecated.

## 0.0.10

### Patch Changes

- c8f2488: build npm package with esbuild instead of vite. Vite does not build isomorphic packages correctly, in particular the dependency to axios

## 0.0.9

### Patch Changes

- 2e1c055: Axios causes some trouble when used NodeJS / CommonJS. Any code importing `axios` now does so in using the `require()` syntax

## 0.0.8

### Patch Changes

- 03562af: Build in CommonJS and ESM instead of UMD and ESM as the UMD bundle generated by the default Vite lib build mode doesn't work with NodeJS

## 0.0.7

### Patch Changes

- 7c3a7be: Remove http timeout options (fix[#157](https://github.com/nhost/nhost/issues/157))
  This new release also comes up with both ESM and CommonJS distributions and solves [#151](https://github.com/nhost/nhost/issues/151)
