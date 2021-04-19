# Hyperlinks

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)

## Intro

Hyperlinks link documents to other documents/resources, link to specific parts of documents, or make apps available at a web address. Web content can be converted to a link so that when clicked/activated, the browser goes to another web address.

URLs can point to:

* HTML files
* text files
* images
* text documents
* videos
* audio files
* anything else on the web

## Anatomy of a Link

Links are wrapped in `<a>` elements, using the
`href` attribute (aka Hypertext Reference/Target) that contains the web address.

```html
<p> Click <a href="https://google.com">Here</a>.</p>
```

> Click [Here](https://google.com).

## Block Level Links

Block-level elements can be made into a link.

```html
<a href="https://google.com">
    <img src="https://cdn.worldvectorlogo.com/logos/google-icon.svg" alt="google logo">
</a>
```

[![Google](https://cdn.worldvectorlogo.com/logos/google-icon.svg)](https://google.com)

## URL/path primer

URL (aka Uniform Resource Locator) is text that defines where something is located on the web.
URLs use paths to find files. Paths define where the file is located in the filesystem.
The __root__ of the structure contains the entire site. Usually there is a file called `index.html` that holds the main page of the site.

Pointing to files:

* Same directory: `<a href="file.html"></a>`
* Subdirectory: `<a href="dir/file.html"></a>`
* Parent directory: `<a href="../pdfs/project.pdf"></a>`

## Document Fragments

You can link to a specific location in an html document. To do this, you must assign
an `id` attribute to the element you want to link to.

```html
<h1 id="page_title">Home</h2>
```

To link to the id, include it at the end of the URL, preceded by a hashtag.

```html
<p><a href="contacts.html#Mailing_List">Mailing List</a></p>
```

Use the fragment alone to link to a place on the current page.

```html
<p>Go <a href="#page_title">Home</a>
```

__Example:__ [Top of this page](#hyperlinks)

## Absolute vs Relative URLs

### Absolute URL

Points to a direct location on the web, including the protocol and domain name.

Example: <https://www.google.com/index.html>

### Relative URL

Points to a location relative to the file you're linking from

Example: [../../../README.md](../../../README.md#web-development-notes)

## Link Best Practices

### Use clear link wording

* Screenreader users like jumping to different links on the page, and reading links out of context.
* Search engines use link text to index target files
* Visual readers skim over the page, eyes will be drawn to page features like links

```html

<!-- Good link text -->
<a href="https://firefox.com">
    Download Firefox
</a>

<!-- Bad link text -->
<p>
    <a href="https://firefox.com">
        Click here
    </a>
to download Firefox.
</p>
```

Tips:

* Don't repeat the URL in the link text.
* Don't say "link" or "links"
* Keep the text as short as possible.
* Minimize multiple copies of the same text linked to different places.
* Use relative links for locations in the *same website.*
  * It's easier to scan code
  * It's more efficient to use relative URLs wherever possible.

## Linking to non-html resources

Make sure to add clear wording to reduce confusion.

For example:

* If you're on low bandwidth, click a link, then a large download starts.
* If you don't have flash installed, click link, then get taken to pager that requires flash

Good Examples:

```html
<p><a href="https://www.example.com/large-report.pdf">
    Download sales report (PDF, 10MB)
</a></p>
```

### Download attribute

When linking to a download, use the `download` attribute to provide a default save
filename.

```html
<a href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=en-US"
   download="firefox-latest-64bit-installer.exe">
  Download Latest Firefox for Windows (64-bit) (English, US)
</a>
```

## Email Links

```html
<a href="mailto:nowhere@example.com">Send email</a>
```

You can omit the email address for "share" links, so users can send an email
to the address of their choosing.

You can also provide other information, including the subject, cc, and body.
Make sure each field is URL encoded, with nonprinting characters.
Use [percent-escaped](https://en.wikipedia.org/wiki/Percent-encoding)
characters where spaces, tabs, etc. are used. Use `&` to separate each field.

```html
<a href="mailto:mail@example.com?cc=name@example.com&bcc=name2@example.com&subject=Hello&body=World">Mail</a>
```

Example: [Mail](mailto:mail@example.com?cc=name@example.com&bcc=name2@example.com&subject=Hello&body=World)
