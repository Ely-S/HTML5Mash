# HTML5Mash 
*A -project in the works- more advanced project template based on HTML5Boilerplate integrated into Twitter Bootstrapp with a few improvements.*


<a href="https://github.com/Ely-S/html5mash/archive/master.zip" title="download"><img style="border: 0px solid black;" src ="https://raw.github.com/Ely-S/html5mash/master/html5.PNG" title="Download!" height="400px"/></a>

## Overview

* Based on Less
* The Bootstrap 2.2.2, JQuery 1.8.3, and HTML5Boilerplate 4.0.3
* HTML5Boilerplate's print styles
* Bootstrap + HTML5Boilerplate index.html template
* Respond.js and HTML5Shim+HTML5printshiv
* HTML5Boilerplate script.js, plugins.js, and style.css templates
* Mixins for Less
* Background patterns
* Better IE classes
* Included docs
* Lightweight development server for Windows
* Sticky Footer component

##Download
CLICK THE BIG 5

##Docs

## Less
HTML5Mash uses Less.  The styles.less file is compiled to style.css.

There are three less files imported into your styles.less file: `stylesheets/components`, `stylesheets/responsive` and `stylesheets/print`.

`stylesheets/components` contains all the Twitter Bootstrap and additional components.  **All it does is import a less file containing styles for each  component** so you remove components from your stylesheet by commenting out import statements.  

`stylesheets/responsive` makes contains Bootstrap's Responsive styles.  **All it does is import a less file containing styles for each screen-width**.  

`stylesheets/print` contains the print styles from HTML5Boilerplate.  

`stylesheets/dss` contains useful mixins from [Less DSS](http://mrkrupski.github.com/LESS-Dynamic-Stylesheet/)

## Javascript

Script are organized like this.

	JS 	-> 	
			Libs		->
							jquery-1.8.3.min.js
							bootstrap ->
											Twitter Bootstrap's Javascript Plugins

			polyfills	->  
							jquery.placeholder.min.js
							respondshiv.min.js
			loader.js
			plugins.js
			script.js


The bootstrap.js file that ships with every download of Twitter Bootstrap contains all of Bootstrap's JQuery plugins in one file, but there is little chance that anyone needs them all.  We only load HTML5Boilerplate's plugins.js and so can put the plugins you need in it to load them all at once.

`respondshiv.min.js` containes Respond.js, HTML5Shiv and HTML5Printshiv so IE parses basic media-queries and displays HTML5 elements correctly.

JQuery.placeholder.min.js is a pollyfill for the placeholder attribute on input tags used in the example feature detect.

####Script Loading

Script loading is done in the `loader.js` file.
The default scipt loader is [Yepnope](http://yepnope.js/), (A.K.A .Modernizr.load) beause it is small and fast.

It would ship with Modernizr but there is no telling what features you will use.  You can start with Yepnope and seamlessly drop in a custom build of Modernizr later.

Personally, I like doing my own feature detects so Yepnope is more than enough.

See Also 

1. http://diveintohtml5.info/everything.html
2. http://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills

## Using Less
####*you must have Less installed*

For Windows users who do not like the command line, doubleclick the Compile.bat file.  It contains the same command needed on Unix systems to compile the Less.

`lessc -x style.less > ../css/style.css`

It would be clever to replace it with your own compile script, e.g.

    lessc -x style.less > ../css/style.css
    yui-compressor -o ../css/style.min.css ../css/style.css

See also

1. Simpless http://wearekiss.com/simpless

## Sticky Footer

The Sticky Footer is a unique component based off work by [Ryan Fait](http://ryanfait.com/sticky-footer/).  It a particularly troublesome to implement and fairly common.  This is how it works.

	<body>
	  <div id="wrapper">
        <div class="container">
          <h1>Title</h1>
        </div>
	    <div id="push"></div>
      </div>
	  <footer id="footer">
	    <div class="container">               
 	    </div>
	  </footer>
	</body>

Everything in the body but the footer goes in a div with a `id="wrapper"`, the last element of which is a div with `id="push"`.  The footer is a footer element with `id="footer"`.

It uses the following variables defined in `variables.less`

	@footerBackground: lighten(@grayLighter, 2%);
	@footerHeight: 80px;

## HTML Classess

    <!doctype html>
    <!--[if lt IE 7]>  <html class="no-js ie ie6 lte7 lte8 lte9">   <![endif]-->
    <!--[if IE 7]>     <html class="no-js ie ie7 lte8 lte9">        <![endif]-->
    <!--[if IE 8]>     <html class="no-js ie ie8 lte9">             <![endif]-->
    <!--[if IE 9]>     <html class="no-js ie ie9">                  <![endif]-->
    <!--[if !IE]><!--> <html class="no-js no-ie">                   <!--<![endif]-->

http://paulirish.com/2008/conditional-stylesheets-vs-css-hacks-answer-neither/

HTML5Mash takes HTML5Boilerplate's IE conditional classes another step and lets you target individual IE versions.

The `no-js` class is replaced by the `js` class if Javascript is detected.

### Web Server

HTML5Mash comes with a very small, windows-only web server for testing purposes and demos.

**[Mongoose](https://github.com/valenok/mongoose) for Windows**

_On Linux try, try `$ python -m SimpleHTTPServer`_

Just double click mongoose.exe and it will serve up your site at port 8080.

From the Mongoose website
> Mongoose executable does not depend on any external library or configuration. If it is copied to any directory and launched from there, it starts to serve that directory on port 8080 (so to access files, go to http://localhost:8080). If some additional config is required - for example, different listening port or IP-based access control, then a mongoose.conf file with respective options can be created in the same directory where executable lives. This makes Mongoose perfect for all sorts of demos, quick tests, file sharing, and Web programming.


## Other

The center tag has been depreciated.  The a utility class `.center` centers elements with set widths. 

Using the noscript tag is an [unreliable way to detect javascript.](http://www.tigerheron.com/article/2007/10/alternative-noscript-tag).  You can use the `.noscript` class instead of basic noscript tags to more reliable determine if javascript runs.

	<div class="noscript>Please Enable Javascript</div>
    
See Also 

1. http://www.w3.org/Style/Examples/007/center.en.html
2. http://www.tigerheron.com/article/2007/10/alternative-noscript-tag


## Logo

To support HTML5, put an [HTML5 logo](http://www.w3.org/html/logo/) on your website.  They are licensed under a [Creative Commons Attribution 3.0 Unported License.](http://creativecommons.org/licenses/by/3.0/)
