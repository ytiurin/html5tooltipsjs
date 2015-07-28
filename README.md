html5tooltips.js
===============
Light and clean tooltips written in pure JavaScript with CSS3 animation and no framework dependencies. [http://ytiurin.github.io/html5tooltipsjs](http://ytiurin.github.io/html5tooltipsjs)

###Simple usage

The simplest way to tie tooltip text to a specific UI element is by adding the data-* attribute to an HTML element.

```html
<span id="refresh" data-tooltip="Refresh"></span>
```

###Advanced usage

You may use a JavaScript constructor. By doing it this way, you have access to a far more flexible and configurable approach.

```javascript
html5tooltips({
  contentText: "Refresh",
  targetSelector: "#refresh"
});
```

Use CSS selectors to tie tooltips to DOM elements. You can make a tooltip stick to any side of the target element.

```javascript
html5tooltips({
  contentText: "Refresh",
  stickTo: "right",
  targetSelector: "#refresh"
});
```

Add explanation text to a tooltip, which shows up when a user focuses on a target element. This feature is designed to explain text input fields and editable elements. You can use HTML formatting.

```javascript
html5tooltips({
  contentText: "Not less then 8 symbols",
  contentMore: "Use lower and UPPER case letters, num<span style='color:red'>6</span>ers and spec<span style='color:red'>!</span>al symbols to make password safe and secure.",
  maxWidth: "180px",
  targetSelector: "#password"
});
```

Define multiple tooltips by submitting each tooltip as an object in a parameter array.

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

Refresh tooltips when you update declarative announcement of tooltips or when DOM change, affecting tooltips target elements.

```javascript
html5tooltips.refresh();
```

###List of possible parameters

- **animateFunction** - Choose one of the available animate functions: ``fadein``, ``foldin``, ``foldout``, ``roll``, ``scalein``, ``slidein``, ``spin``
- **color** - Choose one of the available predefined colors: ``daffodil``, ``daisy``, ``mustard``, ``citrus-zest``, ``pumpkin``, ``tangerine``, ``salmon``, ``persimmon``, ``rouge``, ``scarlet``, ``hot-pink``, ``princess``, ``petal``, ``lilac``, ``lavender``, ``violet``, ``cloud``, ``dream``, ``gulf``, ``turquoise``, ``indigo``, ``navy``, ``sea-foam``, ``teal``, ``peacock``, ``ceadon``, ``olive``, ``bamboo``, ``grass``, ``kelly``, ``forrest``, ``chocolate``, ``terra-cotta``, ``camel``, ``linen``, ``stone``, ``smoke``, ``steel``, ``slate``, ``charcoal``, ``black``, ``white``, ``metalic-silver``, ``metalic-gold``, ``metalic-copper``; or any CSS color.
- **contentText** - Text for a tooltip; HTML may be applied.
- **contentMore** - Text for the expanded version of a tooltip which shows up when focused on a target element; HTML may be applied.
- **disableAnimation** - Disable the animation: ``true`` or ``false``
- **stickTo** - Choose one of the available stick values: ``bottom``, ``left``, ``right``, ``top``
- **stickDistance** - The ``number`` of pixels that represent the distance between the tooltip and a target element.
- **targetSelector** - A CSS selector which is used to catch a target element in the document.
- **targetXPath** - An xPath value which is used to catch a target element in the document.
- **maxWidth** - The maximum width of the expanded version of the tooltip.

###List of possible data-* attributes

- **data-tooltip** - Value for the **contentText** parameter.
- **data-tooltip-animate-function** - Value for the **animateFunction** parameter.
- **data-tooltip-color** - Value for the **color** parameter.
- **data-tooltip-more** - Value for **contentMore** parameter.
- **data-tooltip-stickto** - Value for **stickTo** parameter.
- **data-tooltip-maxwidth** - Value for **maxWidth** parameter.

###Browser compatibility

Tooltips are compatible with old browsers including IE7. Animation works in Chrome 1.0, Firefox 2.0, Internet Explorer 10, Opera 10.5, Safari 3.2.
