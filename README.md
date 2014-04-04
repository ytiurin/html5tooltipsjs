html5tooltips.js
===============
Fast and responsive tooltips with native javascript and CSS3 animation. Perfect for explaining UI elements and controls.

###What's the story?

Designing a website with a pleasant user experience requires attention to details. This often happens when your website should give users an abitily to do hard things by a simple way. Giving a small explanation text to UI elements may become the clue to a winning design. It won’t necessarily make your website a huge success, but it’ll definitely make users appreciate the care you put into your website.

###How it works

html5tooltips.js can be described as an isolated layer that covers the website pages. It contains a number of hidden text boxes, that shows only when user need some hints or explanation. You could find those kind of tooltips when using popular cloud services like Google Mail or Github. It's very intuitive and in most cases you won't realize it's there, until you pay attention. Those small helpers actually do a great job on keeping users confident in your website environment.  

###Installation

Putting tooltips to your website is quite easy. You just need to tie а tooltip text to exact UI element. You can do this by using CSS selectors or by simply adding data-* attribute to an element HTML representation.

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
