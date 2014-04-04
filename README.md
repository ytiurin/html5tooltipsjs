html5tooltips.js
===============
Fast and responsive tooltips with native javascript and CSS3 animation. Perfect for explaining UI elements and controls.

###What's the story?

Designing a website with a pleasant user experience requires attention to details. This often happens when your website should give users an abitily to do hard things by a simple way. Giving a small explanation text to UI elements may become the clue to a winning design. It won’t necessarily make your website a huge success, but it’ll definitely make users appreciate the care you put into your website.

###How does it work?

html5tooltips.js can be described as an isolated layer upon the web document and starts after the page is loaded. Putting tooltips to your website is quite easy. You just need to tie а tooltip text to exact UI element. You can do this by using CSS selectors or by simply adding data-* attribute to an element HTML representation.

```javascript
html5tooltips({
  contentText: "Short and easy to remember",
  targetSelector: "#name"
});
```

or

```html
<input id="name" type="text" data-tooltip-text="Short and easy to remember" />
```
