---
layout: post
title: "Use gulp-sass"
date: 2016-05-09
categories: Test
---

> Tip

if `bower install` not end, use `bower install `

> need to use `@import` to import `.scss` file

```
var sassOptions = {
    style: 'expanded',
    includePaths: ['bower_components']
  }

gulp.src('**/*.scss')
  .pipe($.sass(sassOptions))
  .pipe(gulp.dest('app.css'))
```
