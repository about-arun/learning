# Web Development Bootcamp 2022 Notes

## HTML

### HTML: Essentials

```html
<b></b>
```

> Bring attention to element.

---

```html
<p></p>
```

> Paragraph

---

```html
<h1></h1>
<h2></h2>
<h3></h3>
```

> - advisable to have only one h1 in a page
> - never have a h3 without h2 or h1.

---

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

> Unordered list

---

```html
<ol>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ol>
```

> Ordered List

> - `<ul>` and `<ol>` are supposed to have `<li>` nested under them but `<li>` can have all other elements nested under it.

---

```html
<a href="https://www.google.com">some text</a>
<a href="about.html">some text</a>
<a href="mailto:m.bluth@email.com">some text</a>
<a href="tel:+91857384758">some text</a>
```

> **Anchor tag:** creates a hyperlink to webpages, files, email addresses, locations in same page.

---

```html
<img
  src="https://en.wikipedia.org/wiki/File:FullMoon2010.jpg"
  alt="image description"
  height="500px"
  width="500px"
/>
```

> **Image element** with its common attributes

---

```html
<!-- this is a comment section -->
```

> HTML comments

---

```html
<div></div>
<div class=""></div>
```

> - The Content Division element
> - generic container to hold things or group things together
> - _**block level**_ element

---

```html
<span></span> <span class=""></span>
```

> - container element

> - _**inline**_ element

---

```html
<hr />
```

> horizontal line - represents a thematic break betweek paragraph level elements

---

```html
<br />
```

> line break

---

```html
<sup></sup>
```

> superscript

---

```html
<sub></sub>
```

> subscript

---

### HTML Boilerplate

```html
<!DOCTYPE html>
<html>
  <head>
    <title></title>
  </head>
  <body></body>
</html>
```

> - `<html>` is the root (top-level) element.
> - all other elements must be descentants of `<html>`
> - `<head>` contains metadata
> - `<title>` document's title which appears on the tab of the browser and google uses `<title>` element to list it on the results.

---

### HTML Entities

```html
&#169
```

> - Start with an ampersand and end with a semicolon
> - Used to display reserved characters, that normally would be invalid.
> - Also used in place of difficult to type characters
> - the browser interprets them and renders the correct character instead.
> - Entities list with their codes [link1](https://dev.w3.org/html5/html-author/charref) and [link2](https://entitycode.com/)

---

### Semantic Markup

> - Search engines will consider its contents as important keywords to influence the page's SEO.
> - Accessibility: for screen readers.
> - makes it easy for developers

```html
<section></section>

<nav></nav>

<header></header>

<footer></footer>

<summary></summary>

<details></details>

<time datetime="2018-7-07">July 7</time>

<figure>
  <img src="" />
  <figcaption>The moon</figcaption>
</figure>
```

```html
<article></article>
```

> - Represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable

```html
<main></main>
```

> - `<main>` is the dominant content of the `<body>` of the document.
> - Content that is repeated across a set of documents like sidebars, nav links, copyright, site logos and search forms _**should'nt**_ be included in the `<main>` element.
> - `<main>` does'nt affect the DOM,s concept of the structure of the page.

```html
<aside></aside>
```

> - represents a portion of a document whose content is only indirectly related to the document's main content Asides are frequently presented as sidebars or call-out boxes.

---

### HTML: Tables

```html
<table></table>

<td></td>
- table data cell element: a single cell that contains data

<tr></tr>
- defines a row of cells in a table

<thead></thead>

<tbody></tbody>

<tfoot></tfoot>

<colgroup></colgroup>

<caption></caption>
```

```html
<th></th>
<th scope="col" rowspan="2"></th>
<th scope="col" colspan="2"></th>
```

> - defines a cell as header of a group of cells.
> - The nature of this group is defined by the scope and headers attributes.

---

### HTML: Forms

```html
<form action="server url"></form>
```

> - Represents a document section containing interactive controls for submiting information
> - The `action` attribute specifies WHERE the form data should be sent.
> - The `method` attribute specifies which HTTP method should be used.

---

```html
<input type="text" placeholder="username" name="" id="" />
```

> - used to create a variety of different form controls
> - 20+ possible types of input available
> - type attribute dramatically alters the input's behavior and appearance.
> - only one element on a page should have the given ID.
> - the `name` attribute should match what the server expects to be sent. if the server looks for `search?q` name of this input in this form should be `q`.

---

```html
<input type="checkbox" id="chkyes" name="yes" checked />
```

> `checked` keeps the checkbox checked by default.

---

```html
<label for="some id">Do you like cheese?</label>
```

> - A lable text is both visually and programmatically associated with its text input.
> - a screenreader will read out the lable when the user is focussed on the form input.
> - It increases the hit area for anyone trying to activate the input including those using a touch screen device.

---

```html
<button>Submit</submit>
<button type="button">Submit</submit>
<button type="submit">Submit</submit>
<input type="submit" value="click me!">

```

> - a button outside the form doesnt submit the form by default
> - inside a form, when `type` is not mentioned, the default behavior is `sumbit`.
> - when `type` is set to `button` it doesnt submit form.
> - `input` element of type `sumbit` can be used, but the text on the button must be changed using the `value` attribute.

---

```html
<input type="radio" name="shirt-size" id="S" value="s" />
<input type="radio" name="shirt-size" id="M" value="m" />
<input type="radio" name="shirt-size" id="L" value="l" />
```

> A group of redio buttons share the same `name` attribute that way we can only select one of the radio button.

---

```html
<select name="pets" id="pet-select">
  <option value="" selected>--Please choose--</option>
  <option value="dog">Dog</option>
  <option value="cat">Cat</option>
  <option value="parrot">Parrot</option>
</select>
```

> - Drop down list.
> - including the `selected` attribute makes that option selected by default.

---

```html
<input type="range" name="volume" id="volume" min="0" max="100" step="2" />
```

> - range input is a slider
> - because this type of widget is imprecise, it shouldnt typically be used unless the control's exact value isn't important.

---

```html
<textarea name="feedback" id="feedback" cols="30" rows="5"></textarea>
```

> Multi-line plain-text editing control.

---

### Form Validation

```html
required
```

> - If present, indicates that the user must specify a value for the input before the form can be submitted.
> - `required` attribute is supported by `text, search, url, tel, email, password, date, month, week, time, datetime-local, number, checkbox, radio, file, <input>` types along with the `<select>` and `<textarea>` form controls.
> - It is _**not**_ supported on any of the button types, `image` as well as on `hidden` as it cannot be expected that a user to fill out a form that is hidden
> - It is not relevant to `range` and `color`, as both have default values.

---

```html
minlength maxlength
```

> - defines the minimum number of characters the user can enter into an `<input>` or `<textarea>`.

---

## CSS

### CSS:basics

```css
selector {
  property: value;
}
```

> "**;**" semicolons is a must at the end of CSS property values.

---

```html
<head>
  <link rel="stylesheet" href="app.css" />
</head>
```

> Used to link the css style sheet to the .html document.

---

```css
h2 {
  color: purple;
  background-color: teal;
}

p {
  color: #ffffff;
  background: rgb(89, 151, 0);
}
```

> `background-color` can change just background color whereas `background` can be used to change a lot more like image, gradient. etc.,

---

_**Named colors**_

```css
MediumVioletRed, LightSalmon, PaleGoldenrod ...
```

> Modern browsers support 140 named colors, which are listed in this [link.](https://htmlcolorcodes.com/color-names/)

---

### CSS: Text

```css
text-align: left;
text-align: right;
text-align: center;
text-align: justify;
```

> The `text-align` CSS property sets the horizontal alignment of a block element or a table-cell box.

---

```css
font-weight: normal;
font-weight: bold;
font-weight: lighter;
font-weight: bolder;
font-weight: 100;
font-weight: 900;
```

> - set a the weight (or boldness) of the font. The weights available depend on the `font-family` you are using.
> - typically `font-weight: 400; ` is normal
> - `font-weight: 700; ` is bold

---

```css
text-decoration: underline;
text-decoration: underline dotted;
text-decoration: underline dotted red;
text-decoration: green wavy underline;
text-decoration: underline overline #ff3028;
text-decoration: none;
```

> `none` can be used to remove default underline for example from `anchor` tags.

---

```css
line-height: normal;
line-height: 2.5;
line-height: 3em;
line-height: 150%;
line-height: 32px;
```

---

```css
font-size: 1.2em;
font-size: x-small;
font-size: smaller;
font-size: 12px;
font-size: 80%;
```

> avoid using font-size unit as `px` for responsive web design.

---

```css
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: none;
text-transform: full-width;
text-transform: full-size-kana;
```

---

```css
font-family: Georgia, serif;
font-family: "Gill Sans", sans-serif;
```

> - `Gill Sans` is the primary font and `sans-serif` is the fallback font.
> - A complete collection of web safe CSS font stacks and how much % of windows and Mac machines have it. [Link here](https://www.cssfontstack.com/)

---

### CSS: Selectors

```css
* {
  color: black;
}
```

> _**Universal selector**_ selects everything in the document.

---

```css
img {
  width: 100px;
  height: 200px;
}
```

> _**Element selector**_

---

```css
h1,
h2 {
  color: magenta;
}
```

> _**Selector List**_ combine multiple selectors.

---

```css
#logout {
  color: orange;
  height: 200px;
}
```

> _**ID Selector**_ select the element with id of 'logout'

---

```css
.complete {
  color: green;
}
```

> _**Class selector**_

---

```css
li a {
  color: teal;
}
```

> _**Descendant selector**_
>
> - Select all `<a>`'s that are nested or inside `<li>`. In other words, `<a> `that are descendants of `<li>`.
> - the `SPACE` is important.

---

```css
h1 + p {
  color: red;
}
```

> _**Adjacent selector**_ - the "+" sign is called a combinator.

> Select only the paragraphs that are immediately preceded by an `<h1>`.

---

```css
div > li {
  color: white;
}
```

> _**Direct Child**_

> Select only the `<li>`'s that are direct children of a `<div>` element.

---

```css
input[type="text"] {
  width: 300px;
  color: yellow;
}
```

> _**Attribute Selector**_

> Select all input elements where the `type` attribute is set to "`text`".

---

#### CSS:pseudo-class

```css
a:hover {
  color: orange;
}
```

> _**Pseudo-class :hover**_

> Selects any `<a>` element when "hovered".

---

```css
.post button:active {
  background-color: #02c39a;
}
```

> _**Pseudo-class :active**_

> Select all `buttons`(element selector) which are nested or inside(descendant combinator) of a `.post` class (class selector) which are in an `active` state (pseudo class:active)

---

```css
:checked {
  border: 1px solid blue;
}
```

> _**Pseudo-class :checked**_

> Selects any `radio`, `checkbox`, or `option` element that is checked or toggled to an `on` state

---

```css
p:nth-of-type(4n) {
  color: lime;
}
```

> _**Pseudo-class :nth-of-type()**_

> - matches elements of a given type, based on their position among a group of siblings.
> - the `nth-of-type` pseudo-class is specified with a single argument, which represents the pattern for matching elements.

---

#### CSS: Pseudo elements

```css
h2::first-letter {
  font-size: 50px;
}
```

> Keywords added to a selector that lets you select a particular part of selected element(s)

---

```css
::selection {
  background-color: cyan;
}
```

> - Applies styles to the part of a document that has been highlighted by the user (such as clicking and dragging the mouse across text)
> - Only certain CSS properties can be used with `::selection`.
>   - `color`
>   - `background-color`
>   - `cursor`
>   - `caret-color`
>   - `outline` and its longhands
>   - `text-decoration` and its associated properties
>   - `text-emphasis-color`
>   - `text-shadow`
>   - in particular, `background-image` is _**ignored**_.

---

### CSS: Specificity

> It is a measure of how specific a given selector is. The more specific selector "wins".

> **ID > CLASS > Element**

> **Example 1:**

```css
selection p {
  color: teal;
}
```

> | 0            | 0            | 2              |
> | ------------ | ------------ | -------------- |
> | ID selectors | Class,       | Element,       |
> |              | Attribute,   | Pseudo-element |
> |              | Pseudo-class |                |
>
> Total score: **2**

> **Example 2:**

```css
#submit {
  color: olive;
}
```

> | 1            | 0            | 0              |
> | ------------ | ------------ | -------------- |
> | ID selectors | Class,       | Element,       |
> |              | Attribute,   | Pseudo-element |
> |              | Pseudo-class |                |
>
> Total score: **100**

A link to an online [specificity calculator](https://specificity.keegan.st/).

---

### CSS: Box Model

![css-box-model-image](https://github.com/about-arun/learning/blob/f41d6eb55d09e4ffefeb8a9a56592ad302b50365/images/css-box-model.png)
