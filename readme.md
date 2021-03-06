# Molten Leading (plain JS version)

Manually adjusting ```line-height``` for optimum readability across a bunch of media queries is kind of a pain. With Molten Leading you can set a minimum width at which the adjustment starts, a maximum element width where it stops, and a minimum and maximum line height to adjust through.

All the work here is based on [@Wilto’s Molten-Leading](https://github.com/Wilto/Molten-Leading) jQuery version of the plugin.

#### Features:

* Automatically adjust line-height based on element width for optimal readability.
* Works in all major desktop and mobile browsers, including IE 6 and up.
* Free to use in both commercial and non-commercial projects.
* Doesn’t require external JavaScript libraries.
* Weighs only 817 bytes minified and Gzip’ed.
* Supports multiple instances.


## Usage instructions

Following the steps below you should be able to get everything up and running.

1. Link files:
```html
<script src="moltenleading.js"></script>
```

2. Hook up the plugin:
```html
<!-- Put this right before the </body> closing tag -->
<script>
  moltenLeading("h1");
</script>
```

4. Customizable options:
```javascript
moltenLeading("h1", {
  minline: 1.2,  // Minimum line height for the element
  maxline: 1.8,  // Maximum line height for the element
  minwidth: 320, // Minimum element width where the adjustment starts
  maxwidth: 1024 // Maximum element width where the adjustment stops
});
```


## Notes:
* Tested to be working all the way down to IE6. side note: if you need to support IE6 & 7 you’re gonna have to use simple "tag selectors," since the plugin uses getElementsByTagName as a fallback if querySelector isn’t supported.
* Built Progressive Enhancement in mind, so the plugin will silently fail when a browser doesn’t support certain selector (only IE6 & 7).
* There’s <a href="http://viljamis.com/molten-leading/">a demo here</a>.
* Full credits go to both <a href="http://twitter.com/wilto">Wilto</a> who wrote the orinal plugin and to <a href="http://twitter.com/nicewebtype">Tim Brown</a> for <a href="http://nicewebtype.com/notes/2012/02/03/molten-leading-or-fluid-line-height/">the original idea</a>.


## Changelog

`1.02` (2014-06-21) - Adds minified version.

`1.01` (2014-06-21) - Removes unnecessary code.

`1.00` (2014-06-19) - First release.
