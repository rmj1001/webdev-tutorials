# Getting Started

## Anatomy of an HTML element

```html
<p> My cat is very grumpy </p>
```

`<p>`  - opening tag

`</p>` - closing tag

## Nesting elements

```html

<!-- Right Way -->

<p> My cat is <strong>very</strong></p>

<!-- Wrong Way -->

<p> My cat is <strong>very grumpy.</p></strong>
```

## Block vs. Inline Elements

* Block
  * Form a visible block on a page
  * Appears on a new line
  * Structural elements on page
  * Examples:
    * headings
    * paragraphs
    * lists
    * navigation menus
    * footers
* Inline
  * Contained within block elements
  * Surround small parts of a document's content
  * Will not cause a newline to appear
  * Typically used with text
  * Examples:
    * Links (`<a>`)
    * Emphasis (`<em>`)

## Empty Elements

Not all elements follow the pattern of an opening tag, content, and closing tag.

Example:

```html
<img 
src="https://en.wikipedia.org/wiki/Firefox#/media/File:Firefox_logo,_2019.svg"
>
```

## Attributes

Elements can contain attributes

```html
<!-- Attribute -->

<p class="editor-note">test</p>
```

Attributes contain extra information about the element
that won't appear in the content.

Attributes should contain:

* A space between the it and the element name
* Attribute name & equals sign
* Value wrapped in opening/closing quotes

### Boolean Attributes

```html
<!-- Without Boolean -->
<input type="text" disabled="disabled">
```

```html
<!-- With Boolean -->
<input type="text" disabled>
```

## Anatomy of an HTML document

Template:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Template</title>
    </head>

    <body>
        <p>This is a template HTML document.</p>
    </body>
</html>
```

### `<head>` Element

* Container for everything that isn't content
* Examples:
  * CSS styles
  * Character set declaration

### `<body>` Element

* Container for everything displayed on the page
* Examples:
  * Text
  * Images
  * Videos
  * Games
  * Audio

## Whitespace

No matter how much whitespace you use in HTML, the HTML parser will reduce it all down to a single space. Whitespace is only meant to help with code readability.

## Entity references

To include some characters in your code, you must use their
reference equivalent. You risk breaking the document if an element
isn't typed using its references.

| Literal Character | Character Reference Equivalent |
| ----------------- | ------------------------------ |
| `<`               | `&lt;`                         |
| `>`               | `&gt;`                         |
| `"`               | `&quot;`                       |
| `'`               | `&apos;`                       |
| `&`               | `&amp;`                        |

Examples:

```html
<!-- Wrong -->
<p>In HTML, you define a paragraph using the <p> element.</p>

<!-- Right -->
<p>In HTML, you define a paragraph using the &lt;p&gt; element</p>
```

## HTML comments

Comments help developers share knowledge with eachother without
their content showing up on the document. They are also used to document
and make notes on the code. This is helpful if you leave the project, but return
later.

Example:

```html
<p>This isn't a comment</p>

<!-- <p>This is a comment</p> !-->
```
