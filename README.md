##[liteAccordion](http://nicolahibbert.com/demo/liteAccordion/)

liteAccordion is a horizontal accordion plugin for jQuery, originally developed by [Nicola Hibbert](http://nicolahibbert.com/liteaccordion-v2/).

***
###Options

These are the default settings for the liteAccordion plugin:

    containerWidth : 960,                   // fixed (px)
    containerHeight : 320,                  // fixed (px)
    headerWidth: 48,                        // fixed (px)

    headerSelector : 'h2',                  // selector for tab header
    activateOn : 'click',                   // click or mouseover
    firstSlide : 1,                         // displays slide (n) on page load
    slideSpeed : 800,                       // slide animation speed
    onTriggerSlide : function() {},         // callback on slide activate
    onSlideAnimComplete : function() {},    // callback on slide anim complete

    autoPlay : false,                       // automatically cycle through slides
    pauseOnHover : false,                   // pause on hover
    cycleSpeed : 6000,                      // time between slide cycles
    easing : 'swing',                       // custom easing function

    theme : 'basic',                        // basic, dark, light, or stitch
    rounded : false,                        // square or rounded corners
    enumerateSlides : false,                // put numbers on slides
    linkable : false,                       // link slides via hash

    useIE8Images : false,                   // whether to use image replacement for IE8
    imagePath : undefined,                  // folder in which images are located without trailing slash
    imagePrefix : undefined,                // prefix for all header images
    imageType : undefined,                  // type of images used: png, jpg, gif, etc
    imageAlts : []                          // alt tags for header images in same order as headers

***
###Methods

These are the methods for the liteAccordion plugin:

	play									// trigger autoPlay on a stopped accordion
	stop									// stop an accordion playing
	next									// trigger the next slide
	prev									// trigger the previous slide
    gotoslide                               // go to specific slide
    activate                                // enable single or array of slides
    deactivate                              // disable single or array of slides
	destroy									// remove the accordion, destroying all event handlers and styles (unstyled html content will remain)
	debug									// returns a debug object

All of these methods are chainable (i.e. they return the original DOM object) with the exception of the debug method.  To call a method, use:

$('#yourdiv').liteAccordion('play');

To chain methods:

$('#yourdiv').liteAccordion('next').liteAccordion('next');

To pass a variable into a  method:

$('#yourdiv').liteAccordion('gotoslide',1);

or

$('#yourdiv').liteAccordion('deactivate',[2,3]);

###Not Supported/Won't Fix

- IE6
- IE7 & hashchange - if you need this, please use Ben Alman's [jQuery BBQ](http://benalman.com/projects/jquery-bbq-plugin/) plugin.
- the 'stitch' theme has been stripped back for IE depending on the level of CSS support available.