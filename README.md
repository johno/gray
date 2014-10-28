# Gray

<http://www.g-r-a-y-s-c-a-l-e.com>

Try out different grays while prototyping with the switch of a variable.

## Installation

You can install via [bower](http://bower.io):

```
$ bower install --save grayscale
```

Or, you can install via [npm](http://npmjs.org):

```
$ npm install --save gray
```
Or, you can clone the source:

```
$ git clone https://github.com/johnotander/gray.git
```

### Using with rework

Gray integrates with rework, requiring only the rework-npm and rework-vars plugins:

It provides an index.css file, so you can do the following (assuming the gray npm module is installed).

```css
@import "gray";

/* ... */
```

```js
var gulp       = require('gulp'),
    rework     = require('gulp-rework'),
    reworkVars = require('gulp-rework-vars'),
    reworkNPM  = require('rework-npm');

gulp.task('css', function() {
  return gulp.src('your-css-file.css')
    .pipe(rework(reworkNPM(), reworkVars()))
    .pipe(gulp.dest('dist'));
});
```

### Using the SCSS

In your Scss file, you can import furtive:

```scss
@import "/path/to/gray/scss/all";     // For rgba variables.
@import "/path/to/gray/scss/all-hex"; // For hex variables.
```

Or, if you like, you can just import the variables, they're located in the
`scss` directory, like so:

```scss
@import "/path/to/gray/scss/variables";
```

### Using the CSS

Furtive provides four CSS files: `gray.css`, `gray-hex.css`, and their minified versions. In
order to use one, you can add a `<link>` in your `<head>`.

```html
<!DOCTYPE html>
<html>
<head>
  <!-- ... -->
  <link rel="stylesheet" href="/path/to/gray/css/gray.min.css">
  <!-- ... -->
</head>
<body>
  <!-- ... -->
</body>
</html>
```

## Usage

Detailed color examples available at <http://www.g-r-a-y-s-c-a-l-e.com>.

### Variables

If using SCSS, you know have access to the following variables:

```scss
$gray-light-0: #a0a0a0 !default;
$gray-light-1: #a8a8a8 !default;
$gray-light-2: #b0b0b0 !default;
$gray-light-3: #b8b8b8 !default;
$gray-light-4: #c0c0c0 !default;
$gray-light-5: #d8d8d8 !default;
$gray-light-6: #e0e0e0 !default;
$gray-light-7: #e8e8e8 !default;
$gray-light-8: #fafafa !default;
$gray-light-9: #fff !default;

$gray-mid-0: #606060 !default;
$gray-mid-1: #666 !default;
$gray-mid-2: #707070 !default;
$gray-mid-3: #777 !default;
$gray-mid-4: #808080 !default;
$gray-mid-5: #888 !default;
$gray-mid-6: #909090 !default;
$gray-mid-7: #999 !default;
$gray-mid-8: #a0a0a0 !default;
$gray-mid-9: #a8a8a8 !default;

$gray-dark-0: #080808 !default;
$gray-dark-1: #101010 !default;
$gray-dark-2: #1a1a1a !default;
$gray-dark-3: #202020 !default;
$gray-dark-4: #222 !default;
$gray-dark-5: #282828 !default;
$gray-dark-6: #333 !default;
$gray-dark-7: #383838 !default;
$gray-dark-8: #444 !default;
$gray-dark-9: #484848 !default;
```

### Background color

The utility classes for backround color:

```scss
.bg-gray-light-0 { background-color: $gray-light-0; }
.bg-gray-light-1 { background-color: $gray-light-1; }
.bg-gray-light-2 { background-color: $gray-light-2; }
.bg-gray-light-3 { background-color: $gray-light-3; }
.bg-gray-light-4 { background-color: $gray-light-4; }
.bg-gray-light-5 { background-color: $gray-light-5; }
.bg-gray-light-6 { background-color: $gray-light-6; }
.bg-gray-light-7 { background-color: $gray-light-7; }
.bg-gray-light-8 { background-color: $gray-light-8; }
.bg-gray-light-9 { background-color: $gray-light-9; }

.bg-gray-mid-0 { background-color: $gray-mid-0; }
.bg-gray-mid-1 { background-color: $gray-mid-1; }
.bg-gray-mid-2 { background-color: $gray-mid-2; }
.bg-gray-mid-3 { background-color: $gray-mid-3; }
.bg-gray-mid-4 { background-color: $gray-mid-4; }
.bg-gray-mid-5 { background-color: $gray-mid-5; }
.bg-gray-mid-6 { background-color: $gray-mid-6; }
.bg-gray-mid-7 { background-color: $gray-mid-7; }
.bg-gray-mid-8 { background-color: $gray-mid-8; }
.bg-gray-mid-9 { background-color: $gray-mid-9; }

.bg-gray-dark-0 { background-color: $gray-dark-0; }
.bg-gray-dark-1 { background-color: $gray-dark-1; }
.bg-gray-dark-2 { background-color: $gray-dark-2; }
.bg-gray-dark-3 { background-color: $gray-dark-3; }
.bg-gray-dark-4 { background-color: $gray-dark-4; }
.bg-gray-dark-5 { background-color: $gray-dark-5; }
.bg-gray-dark-6 { background-color: $gray-dark-6; }
.bg-gray-dark-7 { background-color: $gray-dark-7; }
.bg-gray-dark-8 { background-color: $gray-dark-8; }
.bg-gray-dark-9 { background-color: $gray-dark-9; }
```

### Text color

The utility classes for text color:

```scss
.gray-light-0 { color: $gray-light-0; }
.gray-light-1 { color: $gray-light-1; }
.gray-light-2 { color: $gray-light-2; }
.gray-light-3 { color: $gray-light-3; }
.gray-light-4 { color: $gray-light-4; }
.gray-light-5 { color: $gray-light-5; }
.gray-light-6 { color: $gray-light-6; }
.gray-light-7 { color: $gray-light-7; }
.gray-light-8 { color: $gray-light-8; }
.gray-light-9 { color: $gray-light-9; }

.gray-mid-0 { color: $gray-mid-0; }
.gray-mid-1 { color: $gray-mid-1; }
.gray-mid-2 { color: $gray-mid-2; }
.gray-mid-3 { color: $gray-mid-3; }
.gray-mid-4 { color: $gray-mid-4; }
.gray-mid-5 { color: $gray-mid-5; }
.gray-mid-6 { color: $gray-mid-6; }
.gray-mid-7 { color: $gray-mid-7; }
.gray-mid-8 { color: $gray-mid-8; }
.gray-mid-9 { color: $gray-mid-9; }

.gray-dark-0 { color: $gray-dark-0; }
.gray-dark-1 { color: $gray-dark-1; }
.gray-dark-2 { color: $gray-dark-2; }
.gray-dark-3 { color: $gray-dark-3; }
.gray-dark-4 { color: $gray-dark-4; }
.gray-dark-5 { color: $gray-dark-5; }
.gray-dark-6 { color: $gray-dark-6; }
.gray-dark-7 { color: $gray-dark-7; }
.gray-dark-8 { color: $gray-dark-8; }
.gray-dark-9 { color: $gray-dark-9; }
```



## License

MIT

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

Inspired by <http://clrs.cc>

Crafted with <3 by [John Otander](http://johnotander.com)([@4lpine](https://twitter.com/4lpine)).
