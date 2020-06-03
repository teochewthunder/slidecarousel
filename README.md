# Slide Carousel

## Images
These are saved in the `img` folder. They need not conform *exactly* to the viewport in terms of dimensions, but it helps.

## HTML/CSS
This consists of the:
- **Viewport**. This is a div that has the `overflow` property set to `hidden`.
- **Content Container**. This contains two content divs which will be populated as dictated by the JavaScript.

## JavaScript
- The carousel code is encapsulated within an object. The `slides` array contains information about the slides, including images and embedded HTML.
- `setContent()` populates the content divs with the appropriate images and HTML.
- `setTransitionSpeed()` ensures that population of the content divs is instant (i.e, speed set to 0) while "sliding" is set to a higher value.
- `setMargin()` will move the Content Container after the content divs has been populated. All this provides the illusion that it's an endless loop of content.
- `animateSlider()` runs every 5 seconds. By default, it tries to slide left, but only after checking that the `canMove` property is `true`. The `canMove` property is set to `false` if the user clicks on the left or right arrows, thus "manually" sliding the carousel. This changes back to `true` after 5 seconds.

**TODO**: Maybe make the intervals configurable as well?
