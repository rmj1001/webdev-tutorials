# Responsive Images

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

## Why Responsive Images?

When you view images on narrower screens, images can get messed up, It can be difficult to see details.

## How to Create Responsive Images

### Resolution Switching: Different Sizes

Two attributes, `srcset` and `sizes` can provide additional
source images along with hints to help the browser pick the right one.

```html
<img 
    srcset="elva-fairy-480w.jpg 480w,
            elva-fairy-800w.jpg 800w"
    sizes="(max-width:600px) 480px, 800px"
    src="elva-fairy-800w.jpg"
    alt="Elva dressed as a fairy"
/>
```

__`srcset`__ defines the set of images the browser chooses between, and what size each image is. Each set of info is separated by one comma.

1. An image filename (`elva-fairy-480w.jpg`)
2. A space
3. The intrinsic width in pixels (`480`)

__`sizes`__ defines a set of media conditions (e.g. screen widths) and indicates which size is best to choose when conditions are true

1. A media condition (`(max-width:600px)`)
2. A space
3. The width of the slot

With these attributes, the browser will:

1. Look at the device width
2. Work out the first true media condition in the sizes list
3. Load the referenced image in the `srcset` list, or the first image bigger than the chosen slot size

### Resolution Switching: Same size, different resolutions

If you support multiple resolutions, you can allow the browser to choose an appropriate resolution with just `srcset` and x-descriptors.

```html
<img
    srcset="elva-fairy-320w.jpg,
            elva-fairy-480w.jpg 1.5x,
            elva-fairy-640w.jpg 2x"
    src="elva-fairy-640w.jpg"
    alt="Elva dressed as a fairy"
>
```

## Art Direction

You can use the __`<picture>`__ element in cases where you want the image to suit different
display sizes.

Example without art direction:

```html
<img src="elva-800w.jpg" alt="Chris standing up holding Elva" />
```

Use __`<picture>`__ to wrap several __`<source>`__ elements.

```html
<picture>
    <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg">
    <source media="(max-width: 800px)" srcset="elva-800w.jpg">
    <img src="elva-800w.jpg" alt="Chris standing up holding Elva">
</picture>
```

In all cases, you must provide an `<img>` element, with `src` and `alt` attributes before `</picture>`. This provides the default case.

## Use modern image formats boldly

```html
<picture>
    <source type="image/svg+xml" srcset="pyramid.svg">
    <source type="image/webp" srcset="pyramid.webp">
    <img src="pyramid.png" alt="regular pyramid built from 4 equilateral triangles">
</picture>
```
