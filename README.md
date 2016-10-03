# Learning Pug

Notes on using pug https://pugjs.org

- Pug was initially named jade but because of copyright issues it was renamed to pug
- pug files end with .pug and its still backwards compatible with .jade
- pug is used from version 2.0 onwards
- pug is white space sensitive
- install using: node -g pug pug-cli
- pug files are compiled into html file
- to compile a pug file do: pug <pugFile.pug>
- it is possible to use pug file directly in browser but you'll need to include the pug standalone file to translate it. this is not a good idea as the standalone is large but rather do the below
- instead compile the pug file into a js file using the below and include the smaller runtime js

```
pug --client --no-debug <filename.pug>
```

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
