# Learning Pug

Notes on using pug https://pugjs.org

- Pug was initially named jade but because of copyright issues it was renamed to pug
- pug files end with .pug and its still backwards compatible with .jade
- pug is used from version 2.0 onwards
- pug is white space sensitive
- install using: node -g pug pug-cli
- pug files are compiled into html file
- to compile a pug file do: pug <pugFile.pug>

### to use pug programmitcally:
```
// add pug as a dependency
var pug = require('pug');

var fn = pug.compile('string of pug or a pug file', option);

//use function to generate html with the html paramters
var html = fn(myModelData);

//function can be used multiple times
var moreHtml = fn(otherModelData);

//html generation can happen in one step (compile and render but compiles always happens so may have performance issues)
var oneStepHtml = pug.render('pug source', merge(options, myModelData));
var anotherOneStepHtml - pug.render('filename.pug', merge(options, myModelData));
```
