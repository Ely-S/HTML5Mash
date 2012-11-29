# HTML5mash

HTML5mash is a project template based on popular popular technologies.  It elegantly combindes HTML5 Boilerplate, Twitter Bootstrap, Jquery, Yepnope, Less or CSS, Respond.js, and HTML5Shim with some tools, docs, and utilities.

HTML5 BOilerplate

>HTML5 Boilerplate is a professional front-end template that helps you build fast, robust, adaptable, and future-proof websites. Spend more time developing and less time reinventing the wheel.*

Twitter Bootstrap
>Sleek, intuitive, and powerful front-end framework for faster and easier web development.*

## Features and Changes

* Twitter Bootstrap 2.1.0, JQuery 1.8.0, and HTML5 Boilerplate 4.0.0
* Custom build of Bootstrap using tools from HTML5 Boilerplate like Normalize.css 1.0.1. and print stlyes
* Use HTML5 elements and media queries across browsers: comes with Respond.js and HTML5Shim in a conditional comment.
* The fast Yepnope script loader for asynchronously loading scripts without the bulkiness of Modernizr
* HTML5 Boilerplate script.js, plugins.js, and style.css templates
* Twitter Bootstrap and HTML5 Boilerplate combined index.html template
* Use CSS or Less
* With Less only build the parts of bootstrap you need
* Mixins for Less provided by Less Elements
* Sublte Background patterns
* Included docs
* Google analytics loaded asynchronously
* HTML5 Boilerplate's utilities combined with bootstrap's utilities
* Twitter Bootrap's defualt styles
* Added Ajax Loading gif
* Lightweight development server for Windows
* And more

##Download

Just click the HTML5Mash.zip file then View Raw and extract it.

##Docs

### Web Server

HTML5mash comes with a very small, windows-only web server for testing purposes and demos.

######Mongoose https://github.com/valenok/mongoose for Windows

To use it just double click mongoose.exe and it will serve your site at port 8080.

From the Mongoose website
> Mongoose executable does not depend on any external library or configuration. If it is copied to any directory and launched from there, it starts to serve that directory on port 8080 (so to access files, go to http://localhost:8080). If some additional config is required - for example, different listening port or IP-based access control, then a mongoose.conf file with respective options can be created in the same directory where executable lives. This makes Mongoose perfect for all sorts of demos, quick tests, file sharing, and Web programming.


### Loading scripts

Script loading is done in the loader.js file.  It is the only Javascript file linked to by the body.

see [Yepnope](http://yepnope.js/)

### Plugins.js

The bootstrap.js file that comes with every download of Twitter Bootstrap just contains all of Twitter Bootstrap's JQuery plugins in one file but there is little chance anyone needs them all.  HTML5mash ships with all of Bootstrapp's plugins and minified versions so you can put the just the ones you need in plugins.js. 

### Using Less
######*you must have Less installed*

You can install less with NPM or Ruby Gems.

If you use Less uncomment the commented-out link in the head of index.html and delete the links to CSS.  Less will combine all the Less files and compile all the style rules into one stylesheet.  Take a look at styles.less in the less folder.  Also, feel free to delete the CSS directory.

For Windows users who do not like the command line just run the Compile.bat file.  It contains the same command as needed on Unix systems to compile the Less.

`lessc style.less > style.css`

### Bootstrap

Twitter Bootstrap is built out of many Less files.  The main Bootstrap file can be found in bootstrap.less.  It imports one Less file per component so just delete the import statements to get the smallest build of Bootstrap you need.  You can also do the same for responsive.less to not adapt for the screen sizes you don't want to support.

### Mixins 

HTML5mash includes the Less mixins that come with Bootstrap in addition to extra mixins from  Less Elements.

See [Less Elements](http://lesselements.com/)

## Contributing

Contribution is appreciated.  Anyone and everyone is welcome to help out.  It would be nice for somebody to make a logo for the project.

##Maintanence

If people use this I will maintain

### License

All of my original working on this project is in the public domain ([See the Unlicense](http://unlicense.org/)).  
Components this work is based upon are under their respective licenses.