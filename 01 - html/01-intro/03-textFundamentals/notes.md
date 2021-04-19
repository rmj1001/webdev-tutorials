# HTML Text Fundamentals

__Lesson:__ [Click Here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals)

## Intro

Structured content makes reading easier and more enjoyable.

In HTML, each paragraph needs to be wrapped in a `<p>` element.
Each header needs to be wrapped in a heading element.

```html
<h1>This is a header.</h1>
<p>This is a paragraph.</p>
```

There are six heading elements. Each element represents a different level of content in the document. `<h1>` is the main heading,
`<h2>` is subheadings, `<h3>` is sub-subheading, etc.

## Why Structure is Necessary

* Users scan web pages quickly to find relavent content, mostly using headings. They should be able to find their information within a few seconds.
* Search engines use heading content as keywords for search rankings.
* Visually impaired people don't read web pages, they listen instead. Screen readers rely on headings to provide these people with a quick way to navigate websites.
* To style with CSS, or script with JS, you need to have elements wrapping relavent content.

## Why Semantics is Necessary

We need to make sure we are using the correct elements, giving content the correct meaning/function/appearance. `<h1>` is a semantic element, which gives the text it wraps around the meaning of "a top level heading on your page."

```html
<h1>This is a top-level heading</h1>
```

Browsers give it a larger font size to look like a heading.
It's semantic value will be used in many ways as well.

## Lists

__Note:__ You can nest lists inside eachother.

### Unordered

Unordered lists are used for items in which the order doesn't matter.

```html
<!-- Unordered List -->
<!-- <ul> defines the list -->
<!-- <li> defines list items -->
<ul>
    <li>Milk</li>
    <li>Eggs</li>
    <li>Bread</li>
    <li>Hummus</li>
</ul>
```

### Ordered

Ordered lists are used for items in which the order matters.

```html
<!-- Ordered List -->
<!-- <ol> defines the list -->
<!-- <li> defines the list item -->
<ol>
    <li>Drive to the end of the road</li>
    <li>Turn right</li>
    <li>Go straight</li>
    <li>Turn left</li>
    <li>The school is on the left in 300 meters</li>
</ol>
```

### Emphasis

Emphasis is used to *stress* certain words, which alters their
meaning subtly. You can nest emphasis and strong elements.

__Element:__ `<em>`

> I am glad you weren't late. </br>
> I am *glad* you weren't *late*.

```html
<p>I am <em>glad</em> you weren't <em>late</em>.</p>
```

### Strong Importance (bold)

This is used for important words.

__Element:__ `<strong>`

> This liquid is __highly toxic.__ </br>
> I am counting on you. __Do not__ be late!

```html
<p>This liquid is <strong>highly toxic.</strong></p>
<p>I am counting on you. <strong>Do not</strong> be late!</p>
```
