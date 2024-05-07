# Drag Scroller

Allows a container to be scrolled horizontally by mouse, equivalent to dragging a touch screen.

## Example

https://woollymittens.github.io/drag-scroller/

## Instructions

``` javascript
import { DragScroller } from "./drag-scroller.js";
```

### Snap Scroll

``` javascript
const snapScroller = new DragScroller({
    container: document.querySelector('.drag-scroller.snap'),
    increments: document.querySelectorAll('.drag-scroller.snap article'),
    snap: { behavior: "smooth", block: "nearest", inline: "start" },
    scrollHandler: () => {},
    interactionHandler: () => {}
});
```

**container : {DOM element}** - The overflow container within which the content scrolls.

**increments : {DOM elements}** - The individual content elements to which the scrolling should be rounded off to.

**snap : {Object}** - Configuration formatted accordion to the [scrollIntoView](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView) method.

**scrollHandler : {Event handler}** - An event handler that triggers whenever the container scrolls.

**scrollHandler : {Event handler}** - An event handler that triggers only when the container is directly operated by mouse or touch.


### Inertia Scroll

``` javascript
const inertiaScoller = new DragScroller({
    container: document.querySelector('.drag-scroller.inertia'),
    decay: 0.9,
    scrollHandler: () => {}
});
```

**decay : {Fraction}** - A factor between 0 (instant) and 1 (forever) that controls the inertia after dragging.

## License

&copy; Maurice van Creij. Licensed under [The MIT License](https://opensource.org/licenses/MIT).
