# Advanced Formatting

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting)

## Description Lists

Description lists mark up sets of items and their descriptions. This includes terms/definitions, Q&As, etc.

You can have multiple descriptions for each term.

```html
<dl>
    <dt>Q&A</dt>
    <dd>An event where a celebrity answers questions from fans.</dd>
    <dt>Urban Dictionary</dt>
    <dd>Joe Mama</dt>
</dl>
```

> <dl>
> <dt>Q&A</dt>
> <dd>An event where a celebrity answers questions from fans.</dd>
> <dt>Urban Dictionary</dt>
> <dd>Joe Mama</dt>
> </dl>

## Quotations

There are 2 different styles of quotations: block and inline.

### Blockquotes

A section of block-level content (paragraph(s), lists, etc.)

__Element:__ `<blockquote>`

__Example:__

```html
<p> Here below is a blockquote...</p>
<blockquote cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote">
<p>
    The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong> (or <em>HTML Block
  Quotation Element</em>) indicates that the enclosed text is an extended quotation.
</p>
</blockquote>
```

> Here below is a blockquote...
>> The __HTML `<blockquote>` Element__ (or *HTML Block Quotation Element*) indicates that the enclosed text is an extended quotation.

### Inline Quotations

They work the same way as blockquotes, but use a different element.

__Element:__ `<q>`

__Example:__

```html
<p>
    The quote element — <code>&lt;q&gt;</code> — is <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended
for short quotations that don't require paragraph breaks.</q>
</p>
```

> The quote element - `<q>` is <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended for short quotes that don't require paragraph breaks.</q>

## Citations

Browsers, screenreaders, etc. don't really use the cite attribute. Browsers don't display its contents.

The `<cite>` element exists, but it's meant to contain the title of the resource being quoted.

## Abbreviations

Wrap around an abbreviation/acronym, and provide a full expansion.

__Element:__ `<abbr>`

```html
<p>
    We use <abbr title="Hypertext Markup Language">HTML</abbr> to structure web documents.
</p>

<p>
    <abbr title="Doctor">Dr.</abbr> Abbott is very professional.
</p>
```

> We use <abbr title="Hypertext Markup Language">HTML</abbr> to structure web documents.
> <abbr title="Doctor">Dr.</abbr> Abbott is very professional.

## Contact Details

```html
<address>
    <p>
        Chris Mills<br>
        Manchester<br>
        The Grim North<br>
        UK
    </p>

    <ul>
        <li>Tel: 01234 567 890</li>
        <li>Email: <a href="mailto:me@grim-north.co.uk">me@grim-north.co.uk</a></li>
    </ul>
</address>
```

<address>
Chris Mills<br>
Manchester<br>
The Grim North<br>
UK

* Tel: 01234 567 890
* Email: [me@grim-north.co.uk](mailto:me@grim-north.co.uk)

</address>

## Superscript/Subscript

Superscripts/Subscripts are used for dates, chemical formulae, mathematical equations, etc.

```html
<p>My birthday is on the 26<sup>th</sup> of February, 2002.</p>
<p>Caffeine's chemical formula is C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>.</p>
<p>If x<sup>2</sup> is 9, x must equal 3 or -3.</p>
```

> My birthday is on the 26<sup>th</sup> of February, 2002. <br/>
> Caffeine's chemical formula is C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>.<br/>
> If x<sup>2</sup> is 9, x must equal 3 or -3.<br/>

## Computer Code

* `<code>` - Generic computer ode
* `<pre>` - Retain whitespace
* `<var>` - Variable names
* `<kbd>` - Keyboard input
* `<samp>` - Code Output

## Time/Date

Markup times and dates in machine-readable format.

```html
<time datetime="2021-04-19">19 April 2021</time>
```

> <time datetime="2021-04-19">19 April 2021</time>
