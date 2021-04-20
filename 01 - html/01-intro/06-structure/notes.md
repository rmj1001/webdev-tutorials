# Document and Website Structure

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)

## Basic Document Sections

<dl>

<dt>Header:</dt>

<dd>
    Usually a big strip across the top with a big heading,
    logo, and perhaps a tagline. This usually stays the same
    from one page to another.
</dd>

<dt>Navigation bar:</dt>

<dd>
    Links to the site's main sections, usually menu buttons, links, or tabs. The content remains consistent from one webpage to another. Many web designers consider it part of the header rather than an individual component, but it's not not a requirement.
</dd>

<dt>Main Content:</dt>

<dd>
    A big area in the center that contains most of the unique content of the page.
</dd>

<dt>Sidebar:</dt>

<dd>
    Peripheral info, links, quotes, ads, etc. It's contextual to what's contained in the main content, but may contain recurring elements.
</dd>

<dt>Footer:</dt>

<dd>
    A strip across the bottom of the page that contains fine print, copyright notices, or contact info. It also contains common information not critical to the website itself. It can also be used for SEO purposes by providing links for quick access to popular content.
</dd>

![Typical Site Layout](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure/sample-website.png)

## Structuring Content

* __header:__ `<header>`
* __navigation bar:__ `<nav>`
* __main content:__ `<main>`
  * __subsections:__
    1. `<article>`
    2. `<section>`
    3. `<div>`
* __sidebar:__ `<aside>` (often placed in `<main>`)
* __footer:__ `<footer>`

## Non-semantic Wrappers

Non-semantic wrappers are used in instances where you just want to group elements together
to affect them all as a single entity or wrap content. This is useful for CSS and JS. The `<div>` and `<span>` elements are used in these instances. You should provide them with a `class` attribute to give them a label.

`<span>` is inline, while `<div>` is block level.

## Linebreaks and Horizontal Rules

These elements are `<br>` and `<hr>`.

`<br>` creates a line break in a paragraph; it's the only way to force rigid structure for fixed short lines.

`<hr>` creates a horizontal rule that denotes a thematic change in the text.

## Planning a simple website

1. Note down what you want to have common to every page.
2. Draw a rough sketch of what you want the structure of each page to look like. Note what each block will be.
3. Brainstorm all other unique content on the website
4. Sort the content into groups for which parts live on different pages (card sorting)
5. Sketch a rough sitemap -- bubble for each page, draw lines to show workflow. Homepage should be in the center, link to most or all other pages.
