'use strict';

const gulp    = require('gulp');
const sass    = require('./build/sass');
const scripts = require('./build/scripts');
const images  = require('./build/images');
const sync    = require('./build/browsersync');

[sass, scripts, images, sync].forEach(task => {
  task(gulp);
});

//[sass, scripts, images].forEach(task => {
  //task(gulp);
//});

  gulp.task('watch', function() {
   // Watch .js files
  gulp.watch('src/js/*.js', ['scripts']);
   // Watch .scss files
  gulp.watch('src/scss/*.scss', ['sass']);
   // Watch image files
  gulp.watch('src/images/**/*', ['images']);
 });


gulp.task('build', ['sass', 'scripts', 'images', 'jekyll-build', 'watch']);
