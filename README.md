html5tooltips.js
===============
Fast and responsive tooltips with native javascript and CSS3 animation. Perfect for explaining UI elements and controls.

###What's the story?

Designing a website with a pleasant user experience requires attention to details. This often happens when your website should give users an ability to do hard things in a simple way. Giving a small explanation text to UI elements may become a clue to a winning design. It won’t necessarily make your website a huge success, but it’ll definitely make users appreciate the care you put into your website.

###How it works

html5tooltips.js can be described as an isolated layer, covering website pages. It contains a number of hidden text boxes, that show up only when user need some hints or explanation. You could find those kind of tooltips, when using popular cloud services like Google Mail or Github. It's very intuitive and, in most cases, inconspicuous, until you realize it's actually there. Those small helpers do a great job on keeping users calm and confident in your website environment.

###Simple usage

Using html5tooltips.js is quite easy. You just need to tie a tooltip text to the exact UI element. You can do this by simply adding data-* attribute to an element HTML representation.

```html
<span id="refresh" data-tooltip-text="Refresh"></span>
```

###Advanced usage

If you want to have a complete control on the process, you better use javascript constructor. It is perfect when you want to isolate tooltips creation from the document itself.

```javascript
html5tooltips({
  contentText: "Refresh",
  targetSelector: "#refresh"
});
```

You may use CSS or Xpath selectors, the best that fits for you.

```javascript
html5tooltips({
  contentText: "Refresh",
  targetXPath: "/html/body/div[1]/span[1]"
});
```

You can make tooltip stick to one of the target sides.

```javascript
html5tooltips({
  contentText: "Refresh",
  stickTo: "right",
  targetSelector: "#refresh"
});
```

You can add even more explanation text to the tooltip. It would appear when user focus on the target element. This best fits to explain text input fields and content editable areas. You can even add html tags to format text and put links inside the tooltip.

```javascript
html5tooltips({
  contentText: "Not less then 8 symbols",
  contentMore: "Use lower and UPPER case letters, num<span style='color:red'>6</span>ers and spec<span style='color:red'>!</span>al symbols to make password safe and secure.",
  maxWidth: "180px",
  targetSelector: "#password"
});
```

Multiple tooltip definition is supported

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
