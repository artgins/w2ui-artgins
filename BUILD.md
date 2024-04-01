How to build w2ui
=================

. First install dependencies:

```shell
    cd w2ui-artgins # move to project source code
    npm install
```

In `gulpfile.js` are the available commands:

```js
exports.default = gulp.series(tasks.clean, tasks.less, tasks.build_es6, tasks.build)
exports.build   = gulp.series(tasks.build_es6, tasks.build)
exports.dev     = tasks.watch
exports.clean   = tasks.clean
exports.pack    = tasks.pack
exports.less    = gulp.series(tasks.less)
exports.icons   = gulp.series(tasks.icons, tasks.less)
exports.locales = tasks.locales
```

. If icons have changed:

```shell
    gulp icons
```

To change the date of .css files then touch the file `src/less/w2ui.less`

. To build (default):

```shell
    gulp
```
