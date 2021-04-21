# Other embedding technologies

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies)

## iFrame

`<iframe>` elements allow you to embed other web docs into your page. This can be used to incorporate videos, comment systems, maps, ads, etc.

iFrames do have security concerns, so be cautious when using them.

Example iFrame:

```html
<iframe src="https://developer.mozilla.org/en-US/docs/Glossary"
        width="100%" height="500" frameborder="0"
        allowfullscreen sandbox
>
    <p>
        <a href="/en-US/docs/Glossary">
            Fallback link for old browsers
        </a>
    </p>

</iframe>
```

__Attributes:__

<dl>

<dt>allowfullscreen</dt>
<dd>The frame can be placed in fullscreen mode</dd>

<dt>frameborder</dt>
<dd>If set to 1, the browser draws a boarder between the frame and other frames. Set to 0 to disable. This isn't recommended anymore.</dd>

<dt>src</dt>
<dd>Set the URL to the source document</dd>

<dt>width/height</dt>
<dd>Specify the width/height of the frame</dd>

<dt>sandbox</dt>
<dd>Request heightened security settings</dd>

</dl>

__Note:__ It's recommended to use JS to set the iframe URL.

### iframe Security Concerns

iframes are common targets for hackers to attack if they want to modify
your webpage, or trick people into revealing sensitive information. Browsers have developed security measures for making iframes more secure, as well as some best practices.

__Best Practices:__

1. Only embed when necessary
2. Use HTTPS
3. Always use the `sandbox` attribute
4. Configure CSP (content security policy) directives

## `<embed>` and `<object>` elements

These are general purpose embedding tools. They can include plugin
technologies (java, flash, PDF), videos, SVGs, images, etc.

It's not recommended to use plugins like java or flash, and PDFs can be linked instead. Using these elements is more of a legacy technology.

Use the following table to determine information about each element.

|                                     | `<embed>`         | `<object>`                |
| ----------------------------------- | ----------------- | ------------------------- |
| URL of embedded content             | `src`             | `data`                    |
| accurate media type                 | `type`            | `type`                    |
| height/width of box                 | `height`, `width` | `height`, `width`         |
| names/values/parameters             | ad hoc attributes | single-tag `<param>`s     |
| independent HTML content (fallback) | not supported     | contained after `<param>` |
