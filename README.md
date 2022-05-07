# Mobile Rules

A page with minimal mobile-first styling using a reset/normalize library followed by some local CSS rules to make the page useable and accessible.

## Rules For Minimum Functionality

1. The page must view well starting at 320px viewport width and above (with **no media queries** affecting layout or font sizes). Note: The iphone 5/SE in Chrome dev tools is 320px wide in profile mode.
2. Line widths and heights must allow for readability.
3. Elements must have room to breath and text **cannot** hug the sides of the device.
4. You must use @import to load one or more Google fonts (no user agent default fonts).
5. You must use @import to load a reset/normalize library from a CDN.
6. The skip link must be hidden but will display when tabbed.
7. Be sure to include accessibility features that are not necessarily present in the default user agent styles or the reset/normalize styles. For example, line-height by default is too small. If your reset/normalize does not fix this, your local code should.
8. You may use fluid type and spacing (See below for code).
9. The nav bar will be simple and remain visible (and not collapse to a hamburger at small widths).
10. Consider using grid and gap to vertically space out elements instead of margins (this protects against margin collapse). And consider using flex on the nav ul.
11. You may give the body a light colored background and a dark font color, as long as the color contrast > 14. (Something other than stark black on stark white actually improves accessibility for most people.)
12. Colors and font sizes should be declared using custom properties.
13. You may style lists.
14.  The only media query will be an @media print following the rules below.
15. If you feel the need to cite a resource, add it to this README.

### @Media Print Rules

1. All text, including links, are black and the background is white.
2. The external link urls are printed after the text of the link.
3. The skip link doesn't print.
4. You will probably have to search for a solution to this. (put a link in the Resources)
5. [How to Emulate Print Rendering by CSS Tricks](https://css-tricks.com/can-you-view-print-stylesheets-applied-directly-in-the-browser/)

---

> NOTE: This challenge is partly an exercise in accessibility and layout. One default property that tends to make layout hard are lists. This is because the position of the list marker (or list style) is, by default, outside of the element. Consider changing the marker to be inside the element.

```css
:where(ul, ol) {
  list-style-position: inside;
}
```

---

### Available Fluid Code Examples

[Andy Bell's spacing.css - Consistent spacing sizes, based on a ratio, with min and max sizes.](https://gist.github.com/cynthiateeters/88825c17225ce01ef7461e3cd22997ca)

[Andy Bell's text-sizes.css - A minimum and maximum text size allows you to pick the right size from a ratio, depending on the context size.](https://gist.github.com/cynthiateeters/5af47329cbe01e4497b3a0647a5aece4)

### Searching for CSS Reset/Normalize Libraries

[Search GitHub](https://github.com/search?o=desc&q=css+normalize&s=stars&type=Repositories)

[Search CDNJS - search for normalize ](https://cdnjs.com/libraries)

---

### Resources

[HTML Content from Style Stage by Stephanie Eckles](https://stylestage.dev)

[Build Excellent Websites by Andy Bell](https://buildexcellentwebsit.es/)

[Code for Bell's Build Excellent Websites (the source for the Fluid CSS code linked above) ](https://glitch.com/edit/#!/build-excellent-websites)

