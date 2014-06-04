# ampersand-dom

Minimal util-layer for applying transformations to DOM.

**Still in a very in-progress-not-sure-if-this-is-a-good-idea type stage.**

**Still needs tests**

It's a pretty thin layer on top of DOM apis, but should work crossbrowser (needs tests still).

It has zero dependencies.

## install

```
npm install ampersand-dom
```

## example

Here are all the methods and their usage:

```javascript

var dom = require('ampersand-dom');


// sets text content of element
dom.text(el, 'set text content');

// uses classList if available
dom.addClass(el, 'someclass');
dom.removeClass(el, 'someclass');

// removes old if found, adds new
dom.switchClass(el, 'oldclass', 'newclass');

// makes sure attribute (with no content) is added
// if exists it will be cleared of content
dom.addAttribute(el, 'checked');

// completely removes attribute
dom.removeAttribute(el, 'checked');

// sets attribute to string value given, clearing any current value
dom.setAttribute(el, 'value', 'the value');

// sets display none
dom.hide(el);

// shows element, trying to determine it's default display state
// based on tagname and getComputedStyle()
dom.show(el);

// sets inner HTML, takes string or DOM
dom.html(el, '<div></div>');
```

## credits

Initially created by [@HenrikJoreteg](http://twitter.com/henrikjoreteg) with much inspiration/discussion with [@philip_roberts](https://twitter.com/philip_roberts).

## license

MIT
