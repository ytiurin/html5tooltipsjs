html5tooltips.js
===============
Fast and responsive tooltips with native javascript and CSS3 animation. Perfect for explaining UI elements and controls.

###What's the story?

Designing a website with a pleasant user experience requires attention to details. This often happens when your website should give users an ability to do hard things in a simple way. Giving a small explanation text to UI elements may become a clue to a winning design. It won’t necessarily make your website a huge success, but it’ll definitely make users appreciate the care you put into your website.

###How it works

html5tooltips.js can be described as an isolated layer, covering website pages. It contains a number of hidden text boxes, that show up only when user need some hints or explanation. You could find those kind of tooltips, when using popular cloud services like Google Mail or Github. It's very intuitive and, in most cases, inconspicuous, until you realize it's actually there. Those small helpers do a great job on keeping users calm and confident in your website environment.

###Installation

Putting tooltips to your website is quite easy. You just need to tie а tooltip text to the exact UI element. You can do this by using CSS selectors or by simply adding data-* attribute to an element HTML representation.

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
