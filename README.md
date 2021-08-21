# Gulp Setting

## Install Plugins

```
$ node -v
$ npm init -y
# $ npm install gulp -g
$ npm install gulp --save-dev
$ npm install [pligins] --save-dev

# $ npm install --save-dev @babel/preset-env
```

## Replace imagemin
[plugin](https://www.npmjs.com/package/gulp-image)

```bash
$ npm install gulp-image --save-dev
```

```javascript:gulpfile.js
const compressImg = () =>
  src(GULP_PATHS.SRC_IMG)
  .pipe(GULP_CHANGED(GULP_PATHS.OUT_IMG))
  .pipe(GULP_IMAGE({
    pngquant: true,
    optipng: false,
    zopflipng: true,
    jpegRecompress: false,
    mozjpeg: true,
    gifsicle: true,
    svgo: true,
    concurrent: 10,
    quiet: true // defaults to false
  }))
  .pipe(dest(GULP_PATHS.OUT_IMG))

```

## Set gulp-slim
[plugin](https://www.npmjs.com/package/gulp-slim)

```bash
$ sudo gem install slim -v '>= 3.0.2'
$ gem update slim
$ npm install gulp-slim --save-dev
```
