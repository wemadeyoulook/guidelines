# HTML


## Syntax
* Use soft tabs with two spaces - they're the only way to guarantee code renders the same in any environment.
* Nested elements should be indented once (two spaces).
* Always use double quotes, never single quotes, on attributes.
* Don't include a trailing slash in self-closing elements—the HTML5 spec says they're optional.
* Don’t omit optional closing tags (e.g. `</li>` or `</body>`).

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body>
    <article class="news-post"></article>
    <footer>
      <p>Copyright 2016</p>
    </footer>
  </body>
</html>
```

## HTML5 standards
Strive to maintain HTML standards and semantics, but not at the expense of practicality. Use the least amount of markup with the fewest intricacies whenever possible.


## Attribute order
Strive to have the HTML attributes in this particular order. In order for it to be easier to read:

* `class`
* `id, name`
* `data-*`
* `src, for, type, href, value`
* `title, alt`
* `role, aria-*`

Classes make for great reusable components, so they come first. Ids are more specific and should be used sparingly (e.g., for in-page bookmarks), so they come second.

```html
<a class="..." id="..." data-toggle="modal" href="#">
  Example link
</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```

## Reducing markup
Whenever possible, avoid superfluous parent elements when writing HTML. Many times this requires iteration and refactoring, but produces less HTML. See following example:

```html
<!-- Not so great -->
<span class="avatar">
  <img src="...">
</span>

<!-- Better -->
<img class="avatar" src="...">
```

## JavaScript generated markup
Avoid writing markup in JavaScript files. It makes it harder to find and harder to edit.

## Boolean attributes
A boolean attribute is one that needs no declared value. XHTML required you to declare a value, but HTML5 has no such requirement.

```html
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
  <option value="1" selected>1</option>
</select>
```

-----
Inspired by http://codeguide.co/
 
