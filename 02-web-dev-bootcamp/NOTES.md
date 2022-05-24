# Web Development Bootcamp 2022 Notes

## HTML

### HTML: Essentials

```html
<b></b>
```

> Bring attention to element.

```html
<p></p>
```

> Paragraph

```html
<h1></h1>
<h2></h2>
<h3></h3>
```

> - advisable to have only one h1 in a page
> - never have a h3 without h2 or h1.

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

> Unordered list

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

```html
<a href="https://www.google.com">some text</a>
<a href="about.html">some text</a>
<a href="mailto:m.bluth@email.com">some text</a>
<a href="tel:+91857384758">some text</a>
```

> **Anchor tag:** creates a hyperlink to webpages, files, email addresses, locations in same page.

```html
<img
  src="https://en.wikipedia.org/wiki/File:FullMoon2010.jpg"
  alt="image description"
  height="500px"
  width="500px"
/>
```

> **Image element** with its common attributes

```html
<!-- this is a comment section -->
```

> HTML comments

```html
<div></div>
<div class=""></div>
```

> - The Content Division element
> - generic container to hold things or group things together
> - _**block level**_ element

```html
<span></span> <span class=""></span>
```

> - container element

> - _**inline**_ element

```html
<hr />
```

> horizontal line - represents a thematic break betweek paragraph level elements

```html
<br />
```

> line break

```html
<sup></sup>
```

> superscript

```html
<sub></sub>
```

> subscript

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

### HTML Entities

```html
&#169
```

> - Start with an ampersand and end with a semicolon
> - Used to display reserved characters, that normally would be invalid.
> - Also used in place of difficult to type characters
> - the browser interprets them and renders the correct character instead.
> - Entities list with their codes [link1](https://dev.w3.org/html5/html-author/charref) and [link2](https://entitycode.com/)

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

### HTML: Forms

```html
<form action="server url"></form>
```

> - Represents a document section containing interactive controls for submiting information
> - The `action` attribute specifies WHERE the form data should be sent.
> - The `method` attribute specifies which HTTP method should be used.

```html
<input type="text" placeholder="username" name="" id="" />
```

> - used to create a variety of different form controls
> - 20+ possible types of input available
> - type attribute dramatically alters the input's behavior and appearance.
> - only one element on a page should have the given ID.
> - the `name` attribute should match what the server expects to be sent. if the server looks for `search?q` name of this input in this form should be `q`.

```html
<input type="checkbox" id="chkyes" name="yes" checked />
```

> `checked` keeps the checkbox checked by default.

```html
<label for="some id">Do you like cheese?</label>
```

> - A lable text is both visually and programmatically associated with its text input.
> - a screenreader will read out the lable when the user is focussed on the form input.
> - It increases the hit area for anyone trying to activate the input including those using a touch screen device.

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

```html
<input type="radio" name="shirt-size" id="S" value="s" />
<input type="radio" name="shirt-size" id="M" value="m" />
<input type="radio" name="shirt-size" id="L" value="l" />
```

> A group of redio buttons share the same `name` attribute that way we can only select one of the radio button.

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

```html
<input type="range" name="volume" id="volume" min="0" max="100" step="2" />
```

> - range input is a slider
> - because this type of widget is imprecise, it shouldnt typically be used unless the control's exact value isn't important.

```html
<textarea name="feedback" id="feedback" cols="30" rows="5"></textarea>
```

> Multi-line plain-text editing control.

### Form Validation

```html
required
```

> - If present, indicates that the user must specify a value for the input before the form can be submitted.
> - `required` attribute is supported by `text, search, url, tel, email, password, date, month, week, time, datetime-local, number, checkbox, radio, file, <input>` types along with the `<select>` and `<textarea>` form controls.
> - It is _**not**_ supported on any of the button types, `image` as well as on `hidden` as it cannot be expected that a user to fill out a form that is hidden
> - It is not relevant to `range` and `color`, as both have default values.

```html
minlength maxlength
```

> - defines the minimum number of characters the user can enter into an `<input>` or `<textarea>`.

---
