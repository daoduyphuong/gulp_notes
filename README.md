# gulp_notes
Some useful notes about gulp

## Installing Gulp
Install global
```
sudo npm install gulp -g
```
Then install to project 
```
npm install gulp --save-dev
```

## Globing in Node
```
*.scss           // Match any file that have ext .scss in root dir
**/*.scss        // Match any file that have ext .scss in root and any child dir
!not-me.scss     // Not match not-me.scss
*.+(scss|sass)   // Match any file have ext .scss or sass
```

## Working with multiple sources in one task
First, install merge-stream
```
npm install --save-dev merge-stream
```
Then in gulpfile.js
```
var gulp = require('gulp');
var merge = require('merge-stream');

gulp.task('test', function() {
  var bootstrap = gulp.src('bootstrap/js/*.js')
    .pipe(gulp.dest('public/bootstrap'));

  var jquery = gulp.src('jquery.cookie/jquery.cookie.js')
    .pipe(gulp.dest('public/jquery'));

  return merge(bootstrap, jquery);
});
```
