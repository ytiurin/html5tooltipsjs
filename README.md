html5tooltips.js
===============
Light and clean tooltips, written in pure javascript with CSS3 animation. No framework dependency.

###Quick introduction

html5tooltips.js create a number of hidden tooltips in your web UI, showing up only when user needs some hints or explanation on specific UI elements. You could see this kind of tooltips, when using Google Mail, Facebook or Github. It's an intuitive and inconspicuous way to keep users calm and confident in your website environment.

###Simple usage

So, you need to tie a tooltip text to a specific UI element. You can do this by simply adding data-* attribute to an element HTML representation.

```html
<span id="refresh" data-tooltip-text="Refresh"></span>
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

###Browser compatibility

Animation works in:
Chrome 1.0, Firefox 2.0, Internet Explorer 10, Opera 10.5, Safari 3.2