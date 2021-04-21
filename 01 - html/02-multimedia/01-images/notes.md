# Images in HTML

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)

## Basics

```html
<!-- Same directory -->
<img src="image.png">

<!-- Subdirectory -->
<img src="images/image.png">

<!-- URL -->
<img src="https://www.example.com/images/dinosaur.jpg">
```

Don't use images on your site unless:

* You own the image.
* You have received explicit, written permission from the image owner.
* You have ample proof that the image is, in fact, in the public domain.

## Alternative Text

Alternative text is useful in these situations:

* Visually impaired users using screen readers
* Spelling of the file/path name broken
* The brower doesn't support the image type
* You want to provide text for search engines

```html
<img src="file.jpg" alt="File cabinet">
```

## Width/Height

```html
<img src="images/file.jpg" width="400" height="341">
```

## Title

```html
<img src="images/dinosaur" title="A T-Rex on display in the natural history museum">
```

__Note:__ Not recommended due to accessibility problems

## Image Annotations

Use HTML `<figure>` and `<figcaption>` elements to provide a semantic container for the figure, as well as a caption, respectively.

```html
<figure>
    <img src="dino.jpg"
         alt="Head and torso of a dino skeleton"
         width="400"
         height="341">
    <figcaption>
        A T-Rex on display in the Manchester University Museum
    </figcaption>
</figure>
```

__Note:__ Figures can be used for code snippets, audio, video, equations, tables, etc.

## CSS background images

You can use CSS to embed images. You can also set a background image behind elements on a page. This should only be used for decoration.

```css
p {
    background-image: url("dino.jpg")
}
```
