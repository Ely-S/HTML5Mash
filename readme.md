# HTML5Mash 

*A more advanced project template based on HTML5Boilerplate integrated into Twitter Bootstrapp and with a few improvements.*


<a href="downlaod"><img style="border: 0px solid black;" src ="./html5.png" title="Download!" height="400px"/></a>

It elegantly combindes HTML5boilerplate, Twitter Bootstrap, Jquery, Modernizr/Yepnope, Less or CSS, Respond.js, HTML5Shim.
 
> HTML5 Boilerplate is a professional front-end template that helps you build fast, robust, adaptable, and future-proof websites. Spend more time developing and less time reinventing the wheel.


## Overview

* Based on Less
* The Bootstrap 2.2.2, JQuery 1.8.3, and HTML5Boilerplate 4.0.2
* HTML5Boilerplate's print styles
* index.html template
* Respond.js and HTML5Shim+htlm5printshiv in a conditional comment so IE behaves.
* Script loader.
* HTML5Boilerplate script.js, plugins.js, and style.css templates
* Mixins for Less provided Less DSS
* Background patterns
* Included docs
* Lightweight development server for Windows

##Download
To Download CLICK THE BIG 5

#Docs

### CSS

There are three less files imported into your styles.less file: `stylesheets/components.less`, `stylesheets/responsive.less` and `stylesheets/print.less`.

`stylesheets/components.less` is based off of the `bootstrap.less` from 
Twitter Bootstrap.  **All it does is import a file for every component** so you can manage the components you want by commenting out the import statements.  It contains three new imports `HTML5Bolerplate.less`, `dss.less` and `footer.less` which cointain the default styles of HTML5Boilerplate, Less Dnamic StyleSheet mixins and the footer component.

`stylesheets/responsive.less` makes it responsive.  **All it does is import a less file for each screen-width**.  You can modify thei mports to include styles for different device widths.

`stylesheets/print.less` is at the end and **contains the print styles from HTML5Boilerplate**.  It should be inlined to avoid another HTTP request.


### Mixins 

[Mixins are included from Less DSS.](http://mrkrupski.github.com/LESS-Dynamic-Stylesheet/)

### Javascript

Javascript is organized like this.

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


The bootstrap.js file that ships with every download of Twitter Bootstrap containes all of Bootstrap's JQuery plugins in one file, but there is little chance that anyone needs all of them.  We only load HTML5Boilerplate's plugins.js and you can put just the plugins you need in it and load them all at once.

respondshiv.min.js containes Respond.js and HTML5Shiv and HTML5 Printshiv so IE parses mediaqueries and desplays HTML5 elements.

JQuery.placeholder.min.js is a pollyfill for the placeholder attribute on input tags used in an example feature detect.

####Script Loading

Script loading is done in the loader.js file.  It is the only javascript file linked to in the head.

The default scipt loader is [Yepnope](http://yepnope.js/) (A.K.A .Modernizr.load) beause it is small and fast.

It would ship with Modernizr but you should use your own custom build.  HTML5 Smash contains Yepnope.js, AKA Modernizr.load, the script loader of Modernizr.  You can use it to conditionally load your scripts in parallel and seamlessly drop in a custom build of Modernizr later.

Personally, I like doing my own feature detects so Yepnope is more than enough.

See Also 

1. http://diveintohtml5.info/everything.html
2. http://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills

### Using Less
######*you must have Less installed*

You can install less with NPM or Ruby Gems.

For Windows users who do not like the command line, doubleclick the Compile.bat file.  It contains the same command as needed on Unix systems to compile the Less.

`lessc style.less > style.css`


It would be clever to replace it with your own compile script.

### Sticky Footer

The Sticky Footer is a unique component based off work by [Ryan Fait]().  It a particularly troublesome to implement and fairly common.  This is how it works.

	<body>
	  <div id="wrapper">
        <div id="content" class="container">
          <h1>Title</h1>
        </div>
	    <div id="push"></div>
      </div>
	  <footer id="footer">
	    <div class="container">
    	  <p>Footer</p>
 	    </div>
	  </footer>
	</body>

Everything in the body but the footer goes in a div with a `wrapper` id, the last element of which is a div with the `push` id.  The footer can be any block-level element with `id="footer"`.

It uses the following variables defined in `variables.less`

	@footerBackground: lighten(@grayLighter, 3%);
	@footerHeight: 80px;

#### HTML Classess

    <!doctype html>
    <!--[if lt IE 7]>  <html class="no-js ie ie6 lte7 lte8 lte9">   <![endif]-->
    <!--[if IE 7]>     <html class="no-js ie ie7 lte8 lte9">        <![endif]-->
    <!--[if IE 8]>     <html class="no-js ie ie8 lte9">             <![endif]-->
    <!--[if IE 9]>     <html class="no-js ie ie9">                  <![endif]-->
    <!--[if !IE]><!--> <html class="no-js no-ie">                   <!--<![endif]-->

http://paulirish.com/2008/conditional-stylesheets-vs-css-hacks-answer-neither/

HTML5Mash takes html5boilerplate's IE conditional stlyehseets another step and lets you target indiivual versions.

The `no-js` class is replaced by the `js` class if
### Other

The center tag has been depreciated.  The a utility class `.center` centers elements with set widths using CSS. See http://www.w3.org/Style/Examples/007/center.en.html

	.center {
    	display: block;
	    margin-left: auto;
    	margin-right: auto;
	}


Using the noscript tag is an [unreliable way to detect javascript.](http://www.tigerheron.com/article/2007/10/alternative-noscript-tag) Since the `.no-js` is on the html5 element if javascript does not run, it can be used to tell wether javascript is enabled. You can use the `.noscript` utility class instead of basic noscript tags.

	<div class="noscript>Please Enable Javascript</div>
    
### Web Server

HTML5Smash comes with a very small, windows-only web server for testing purposes and demos.

**[Mongoose](https://github.com/valenok/mongoose) for Windows**

_Linux Peeps, try `$ python -m SimpleHTTPServer`_

To use it just double click mongoose.exe and it will serve your site at port 8080.

From the Mongoose website
> Mongoose executable does not depend on any external library or configuration. If it is copied to any directory and launched from there, it starts to serve that directory on port 8080 (so to access files, go to http://localhost:8080). If some additional config is required - for example, different listening port or IP-based access control, then a mongoose.conf file with respective options can be created in the same directory where executable lives. This makes Mongoose perfect for all sorts of demos, quick tests, file sharing, and Web programming.


## Logo

To Support HTML5 put the logo on your website.  It is licensed under a [Creative Commons Attribution 3.0 Unported License.](http://creativecommons.org/licenses/by/3.0/)
