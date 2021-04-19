# What is the HTML head?

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)

## Intro

```html
<!-- Template -->

<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>My test page</title>
    </head>
</html>
```

The HTML head is the contents inside the `<head>` element.
It does not display content on the page. It stores metadata
about the document.

## Title

The `<title>` tag is what gives the document its title.
The title is only really displayed in the page's tab.
This shouldn't be confused with the `<h1>` element, which
is used in the body.

The title tag can also be found in search results for the
page.

## Metadata

The metadata describes the data of the document. The element
used for this is `<meta>`. One example of data is the character
set (charset). This describes the type of characters used in the
document. English users will likely use `utf-8`.

Metadata examples:

* charset
* author
* description

Example:

```html
<meta charset="utf-8">
<meta name="author" content="Roy Conn">
<meta name="description" content="Lorem ipsum">
```

You should include the author name for contact purposes. You should
also include a description that includes relavent keywords for your content,
so your page appears higher in search engine rankings (search engine optimization).

## Other types of metadata

Many features on other websites are proprietary creations that provide certain sites
with specific pieces of information they can use (social media for example).

[Open Graph Data](http://ogp.me/) is a protocol from facebook that provides richer
metadata for websites.

[Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards) is a similar protocol to [Open Graph Data](http://ogp.me/) but is used primarily on [Twitter](https://twitter.com).

## Custom Site Icon

You can add references to custom icons in your metadata to enrich your site's design.
The most popular format is the favicon, which has been around for many years. It's a
16-pixel square icon that's used in the browser tab, bookmarks/favorites, etc.

Adding a favicon:

1. Save it in the same directory as the index page, saved as `name.ico`.
2. Add the following line into your HTML's `<head>` block:

```html
<link rel="shortut icon" href="name.ico" type="image/x-icon">
```

## Applying CSS/Javascript to HTML

CSS and javascript are used to enhance webpages. CSS makes them look cool, while
javascript makes the page interactive (think videos, maps, games). These are
commonly applied using the `<link>` element and the `<script>` element, respectively.

* The `<link>` and `<script>` elements should both go in the head of the document.
* The `<link>` includes the `rel="stylesheet"`, and the `href="file.css"` attributes.
* The `<script>` element includes an `src="script.js"` attribute. You can use the `defer` attribute to load the script after the html is rendered.

## Setting the primary language of the document

```html
<html lang="en-US"></html>
```

You can also set subsections of the document to be different languages.

```html
<p>Japanese: <span lang="ja">ご飯が熱い。</span>.</p>
```

Learn more about [Languages Tags](https://www.w3.org/International/articles/language-tags/).
