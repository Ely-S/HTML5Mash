# HTML5mash

HTML5mash is a project template based on popular popular technologies.  It elegantly combindes HTML5boilerplate, Twitter Bootstrap, Jquery, Yepnope, Less or CSS, Respond.js, HTML5Shim.

>HTML5 Boilerplate is a professional front-end template that helps you build fast, robust, adaptable, and future-proof websites. Spend more time developing and less time reinventing the wheel.*

>Sleek, intuitive, and powerful front-end framework for faster and easier web development.*

## Features and Changes

* The Bootstrap 2.1.0, JQuery 1.8.0, and HTML5Boilerplate 4.0.0
* Custom build of bootstrap using tools from HTML5Boilerplate like Normalize.css 1.0.1. and print stlyes
* Use HTML5 elements and media queries across browsers.  This comes with Respond.js and HTML5Shim in a conditional comment.
* The fast Yepnope script loader for asynchronously loading scripts without the bulkiness of Modernizr
* HTML5Boilerplate script.js, plugins.js, and style.css templates
* Twitter Bootstrap and HTML5Boilerplate combined index.html template
* Use CSS or Less
* While using Less, only build the parts of bootstrap you need
* Mixins for Less provided by Less Elements
* Background patterns
* Included docs
* Google analytics loaded asynchronously
* HTMLBoilerplate's utilities combined with bootstrap's utilities
* Twitter Bootrap's defualt styles
* HTML5Boilerplate's hr styles moved into bootstrap's scaffolding
* Added Ajax Loading gif
* Lightweight development server for Windows
* And more

##Docs

### Web Server

HTML5Smash comes with a very small, windows-only web server for testing purposes and demos.

######Mongoose https://github.com/valenok/mongoose for windows

To use it just double click mongoose.exe and it will serve your site at port 8080.

> Mongoose executable does not depend on any external library or configuration. If it is copied to any directory and launched from there, it starts to serve that directory on port 8080 (so to access files, go to http://localhost:8080). If some additional config is required - for example, different listening port or IP-based access control, then a mongoose.conf file with respective options can be created in the same directory where executable lives. This makes Mongoose perfect for all sorts of demos, quick tests, file sharing, and Web programming.


### Loading scripts

Script loading is done in the loader.js file.  It is the only JS file linked by the body.

see [Yepnope](http://yepnope.js/)

### Plugins.js

The Bootstrap.js that comes with ever download of twitter bootstrap is just all of Twitter Bootstrap's JQuery plugins in one file.  There is little chance anyone needs all of them.  This package ships with all of Bootstrapp's plugins with minified versions so you can put the just the ones you need in plugins.js. 

### Using Less
######*you must have Less installed*

You can install less with NPM or Ruby Gems.

If you use Less uncomment the commented-out link in the head of index.html and delete the links to CSS.  The way Less works is that it compiles all the styles into one stylesheet.  Take a look at styles.less in the less folder.  Also, feel free to delete the CSS directory.

For Windows users who do not like the command line just double run the Compile.bat file.  It contains the same command to compile the style.less on Unix systems.

`lessc style.less > style.css`

### Bootstrap

Bootstrap is build out of many Less files.  The main bootstrap file can be found in bootstrap.less.  Delete the import statements you don't need to get the smallest build of bootstrap you need.


### Mixins 

HTML5Smash includes the Less mixins that come with bootstrap and Less elements.

See [Less Elements](http://lesselements.com/)

## Contributing

Contribution is appreciated.  Anyone and everyone is welcome to help out.


### License


All of my original working on this project is in the public domain.  All the components this is based upon are under their respective licenses.