#### Objective: 
To install gulp-responsive, so that I can automatically resize and compress my images into multiple resolutions.

#### Situation:
In Udacity Mobile Web Specialist Nanodegree Part 2 Lesson 7.16 Quiz: Project Part 1, it asks us to use automated tool to process images into different sizes. But we were not shown how to use Grunt. From what I gather I should be learning Gulp instead of Grunt. The reasoning for that is Gulp is covered in Part 3, and people on the Slack channel is recommending Gulp over Grunt.

#### Resources:
- gulp (task runner, automation tool)
- gulp-load-plugins
- sharp
- gulp-responsive
- Watch LevelUpTuts on [youtube](https://www.youtube.com/watch?v=wNlEK8qrb0M&list=PLLnpHn493BHE2RsdyUNpbiVn-cfuV7Fos&index=1)

#### Procedure:
1. Open node.js command prompt.
2. cd into the project directory.
3. run `npm install --save-dev gulp`
4. We can check if gulp is working by first setting up a basic Hello World gulpfile.js, see below.
5. Run `gulp` on command line. The console should output "Hello World".
6. Now we can setup gulp-responsive, in the same project folder. Please follow the order below.
7. Run `npm install --save-dev gulp-load-plugins`
8. Run `npm install sharp`
9. Run `npm install --save-dev gulp-responsive`
10. Update gulpfile.js.
11. Run `gulp images` to start the script.

#### To-do:
Update gulpfile.js to move original images out from images_src into an original folder. Or maybe even delete them. I don't know yet. This looks like a simple task and easy to do, I just need to figure out how I want to handle the original images. [Try this link](http://learningwithjb.com/posts/moving-files-with-gulp).

#### Other comments:

Here's a basic Hello World gulpfile.js:
```
var gulp = require('gulp');

gulp.task('default', function() {
	console.log('Hello World');
});
```
Here's my current gulpfile.js to create multiple resolutions of a single image, 800px and 1600px.
```
var gulp = require('gulp');
var $ = require('gulp-load-plugins')();

gulp.task('images', function () {
  return gulp.src('images_src/*.jpg')
    .pipe($.responsive({
      '*': [
      {
        width: 800,
        rename: {
          suffix: '-800px',
          extname: '.jpg',
        },
        withoutEnlargement: true,
      }, 
      {
        width: 1600,
        rename: {
          suffix: '-1600px',
          extname: '.jpg',
        },
        withoutEnlargement: true,
      }, 

      ],
    }, {
      // Global configuration for all images
      // The output quality for JPEG, WebP and TIFF output formats
      quality: 50,
      // Use progressive (interlace) scan for JPEG and PNG output
      progressive: true,
      // Strip all metadata
      withMetadata: false,
      // Do not emit the error when image is enlarged.
      errorOnEnlargement: false,
    }))
    .pipe(gulp.dest('img'));
});
```
