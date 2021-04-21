# Vector Graphics on the Web

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Adding_vector_graphics_to_the_Web)

## Vector Graphics vs Raster Images

Raster images are a grid of pixels, with information showing exactly where each
pixel is placed. Popular formats include Bitmap (`.bmp`), PNG (`.png`), JPG (`.jpg`), and GIF (`.gif`).

Vector graphics are defined using algorithms. Vector image files contain shape and path definitions that the computer can render at will. The SVG format is the most popular.

Vector graphics can scale on displays without compromising information, while raster images can become pixelated.

## SVG

SVG is an [XML](https://developer.mozilla.org/en-US/docs/Glossary/XML)-based language for describing vector images. It's like HTML, except there are custom elements for all the image effects and shapes.

__Example:__

```svg
<svg version="1.1"
    baseProfile="full"
    width="300" height="200"
    xmlns="http://www.w3.org/2000/svg">
    
    <rect width="100%" height="100%" fill="black" />
    <circle cx="150" cy="100" r="90" fill="blue" />

</svg>
```

SVG has some advantages:

* Text in vector images remains accessible
* SVGs are great for styling/scripting, since components are elements that can be styled via CSS or scripted vs JS.

Raster has advantages:

* SVG can get complicated quickly, with growing filesizes, and complex SVGs taking processing time
* SVG can be harder to create than raster images
* SVG isn't supported in older browsers

## Adding SVG to pages

### The quick way: `<img>`

You can embed an SVG into an `<img>` element, same as other image formats.

```html
<img 
    src="logo.svg"
    alt="A dove with outstretched wings"
    height="50"
    width="50"
/>
```

__Pros:__

* Quick, familiar syntax
* Can make the image a hyperlink
* The SVG file can be cached for faster loading times

__Cons:__

* Cannot manipulate w/ JS
* Must include inline CSS in SVG code to style it
* Cannot restyle the image with CSS pseudoclasses

### Troubleshooting, Cross-Browser Support

Reference a PNG/JPG image in the `src` attribute, and use the `srcset` attribute
to reference the SVG in newer browsers.

```html
<img 
    src="logo.png"
    alt="A dove with outstretched wings"
    height="50"
    width="50"
    srcset="logo.svg"
/>
```

You can also set SVGs as CSS background images

```css
background: url("fallback.png") no-repeat center;
background-image: url("image.svg");
background-size: contain;
```

SVGs inserted with CSS cannot be manipulated with JS or CSS pseudo-classes

### Include SVG code in HTML

You can put raw SVG code in your HTML instead of referencing the file.

__Pros:__

* Saves an HTTP request, saving time
* You can assign classes and ids to SVG
  * Style them in CSS
* This is the only approach that allows CSS interactions/animations on the SVG image
* You can make SVG markup into a hyperlink

__Cons:__

* Only suitable for SVG in one place
* Extra SVG code increases HTML file size
* Browsers cannot cache inline SVG
* You can include fallback in a `<foreignObject>` element, but browsers that support SVG still download fallback images.

### SVG in an iframe

```html
<iframe src="triangle.svg" width="500" height="500" sandbox>
    <img src="triangle.png" alt="Triangle with 3 unequal sides" />
</iframe>
```

__Cons:__

* iframes have a fallback mechanism, but it's only displayed if iframes are not supported.
* Unless the SVG and the webpage have the same origin, you can't use JS on the main webpage to manipulate the SVG.
