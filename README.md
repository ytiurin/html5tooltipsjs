html5tooltips.js
===============
Light and clean tooltips, written in pure javascript with CSS3 animation. No framework dependency.

###Quick introduction

html5tooltips.js create a number of hidden tooltips in your website, showing up only when user needs some hints or explanation on specific UI elements. You see tooltips, when using Google Mail, Facebook or Github. It's an intuitive and inconspicuous way to keep users calm and confident in your website environment.

###Simple usage

The simple way to tie a tooltip text to a specific UI element is by adding data-* attribute to an element HTML representation.

```html
<span id="refresh" data-tooltip="Refresh"></span>
```

###Advanced usage

You may use a javascript constructor itself. It's more flexible and configurable way to use a tool

```javascript
html5tooltips({
  contentText: "Refresh",
  targetSelector: "#refresh"
});
```

Use CSS selectors to tie tooltips to different DOM elements. You can make a tooltip stick to any side of the target element

```javascript
html5tooltips({
  contentText: "Refresh",
  stickTo: "right",
  targetSelector: "#refresh"
});
```

You can add even more explanation text to a tooltip, which shows up only when user focus on a target element. This feature is designed to explain text input fields and content editable areas. You can even use html formatting

```javascript
html5tooltips({
  contentText: "Not less then 8 symbols",
  contentMore: "Use lower and UPPER case letters, num<span style='color:red'>6</span>ers and spec<span style='color:red'>!</span>al symbols to make password safe and secure.",
  maxWidth: "180px",
  targetSelector: "#password"
});
```

Multiple tooltip definition is possible

```javascript
html5tooltips([
  {
    contentText: "Delete",
    targetSelector: "#delete"
  },
  {
    contentText: "Refresh",
    stickTo: "top",
    targetSelector: "#refresh"
  },
  {
    contentText: "Simple to remember",
    contentMore: "Check that your login name is not used by anyone else.",
    stickTo: "left",
    maxWidth: "180px",
    targetSelector: "#username"
  }
]);
```

###List of possible parameters

**animateFunction** one of available animate functions: ``fadein``, ``foldin``, ``foldout``, ``roll``, ``scalein``, ``slidein``, ``spin``  
**color** one of available predefined colors: ``daffodil``, ``daisy``, ``mustard``, ``citrus-zest``, ``pumpkin``, ``tangerine``, ``salmon``, ``persimmon``, ``rouge``, ``scarlet``, ``hot-pink``, ``princess``, ``petal``, ``lilac``, ``lavender``, ``violet``, ``cloud``, ``dream``, ``gulf``, ``turquoise``, ``indigo``, ``navy``, ``sea-foam``, ``teal``, ``peacock``, ``ceadon``, ``olive``, ``bamboo``, ``grass``, ``kelly``, ``forrest``, ``chocolate``, ``terra-cotta``, ``camel``, ``linen``, ``stone``, ``smoke``, ``steel``, ``slate``, ``charcoal``, ``black``, ``white``, ``metalic-silver``, ``metalic-gold``, ``metalic-copper``; or any CSS color  
**contentText** text for a tooltip; html may be applied  
**contentMore** text for expanded version of tooltip which showup whenn focus on target element; html may be applied  
**disableAnimation** disable the animation ``true`` or ``false``  
**stickTo** one of available stick values: ``bottom``, ``left``, ``right``, ``top``  
**stickDistance** a ``number`` of pixels that represent the distance between tooltip and target element  
**targetSelector** css selector which is used to catch a target element in the document  
**targetXPath** xPath value which is used to catch a target element in the document  
**maxWidth** maximum width of expanded version of tooltip

###List of possible data-* attributes

**data-tooltip** value for **contentText** parameter  
**data-tooltip-animate-function** value for **animateFunction** parameter  
**data-tooltip-color** value for **color** parameter  
**data-tooltip-more** value for **contentMore** parameter  
**data-tooltip-stickto** value for **stickTo** parameter  
**data-tooltip-maxwidth** value for **maxWidth** parameter  

###Browser compatibility

Animation works in:
Chrome 1.0, Firefox 2.0, Internet Explorer 10, Opera 10.5, Safari 3.2