# < Wildebeest HTML Style Guide >

*A mostly reasonable approach to HTML*


## <a name='TOC'>Table of Contents</a>
**(Work in progress...)**

### Name your content by HTML structural elements.
Never name your content after the visual appearance but after its description. (e.g. prefer "sidebar-container" than "right-container")

```html
  <body>
    <div class="container">
      <div class="content-container">...</div>
      <aside class="sidebar-container">...</aside>
    </div>
    ...
  </body>
```


### HTML Attributes Naming
Name your id & classes after the elements description and not about the visual elements, use `.external-link` instead of `.red-link` => what if you change the color of the link?
Use hyphen to name your attributes and class.

```html
  <!-- bad -->
  <a href="http://google.com" class="red_link">View article</a>

  <!-- good -->
  <a href="http://google.com" class="external-link">View article</a>
```
  
### Capitalization
All code has to be lowercase: This applies to HTML element names, attributes, attribute values (unless text/CDATA), CSS selectors, properties, and property values (with the exception of strings).

```html
  <!-- bad -->
  <div CLASS="menu">

  <!-- good -->
  <img src="wildebeest.png" alt="Wildebeest">

```

### Spaces and Equal Signs
Space-less is easier to read, and groups entities better together
```html
  <!-- bad -->
  <link rel = "stylesheet" href = "styles.css">

  <!-- good -->
  <link rel="stylesheet" href="styles.css">
```

### Avoid Long Code Lines
When using an HTML editor, it is inconvenient to scroll right and left to read the HTML code.
Try to avoid code lines longer than 80 characters.

### Indentation
Indent using 2 or 4 spaces (choose one of those and keep the same criteria across the project).
Don't use tabs or mix tabs and spaces for indentation.

### Document Type:
HTML5 (HTML syntax) is preferred for all HTML documents: `<!DOCTYPE html>`.
It’s recommended to use HTML, as `text/html`. Do not use XHTML. XHTML, as `application/xhtml+xml`, lacks both browser and infrastructure support and offers less room for optimization than HTML.
Although fine with HTML, do not close void elements, i.e. write `<br>`, not `<br />`.

### HTML Validity
Use valid HTML code unless that is not possible due to otherwise unattainable performance goals regarding file size.
Use tools such as the [W3C HTML validator](https://validator.w3.org/nu/) to test.

### Semantics
Use HTML according to its purpose. Use elements (sometimes incorrectly called “tags”) for what they have been created for. For example, use heading elements for headings, `p` elements for paragraphs, `a` elements for anchors, etc.
Using HTML according to its purpose is important for accessibility, reuse, and code efficiency reasons.

```html
  <!-- bad -->
  <div onclick="goToRecommendations();">All recommendations</div>

  <!-- good -->
  <a href="recommendations/">All recommendations</a>
```

### Multimedia Fallback
Provide alternative contents for multimedia. For multimedia, such as images, videos, animated objects via canvas, make sure to offer alternative access. For images that means use of meaningful alternative text (`alt`) and for video and audio transcripts and captions, if available.

Providing alternative contents is important for accessibility reasons: A blind user has few cues to tell what an image is about without `@alt`, and other users may have no way of understanding what video or audio contents are about either.

(For images whose alt attributes would introduce redundancy, and for images whose purpose is purely decorative which you cannot immediately use CSS for, use no alternative text, as in `alt=""`.)
```html
  <!-- bad -->
  <img src="spreadsheet.png">

  <!-- good -->
  <img src="spreadsheet.png" alt="Spreadsheet screenshot.">
```

### Separation of Concerns
Strictly keep structure (markup), presentation (styling), and behavior (scripting) apart, and try to keep the interaction between the three to an absolute minimum.

That is, make sure documents and templates contain only HTML and HTML that is solely serving structural purposes. Move everything presentational into style sheets, and everything behavioral into scripts.

In addition, keep the contact area as small as possible by linking as few style sheets and scripts as possible from documents and templates.

Separating structure from presentation from behavior is important for maintenance reasons. It is always more expensive to change HTML documents and templates than it is to update style sheets and scripts.

### HTML quotation marks
When quoting attributes values, use double quotation marks. Use double ("") rather than single quotation marks ('') around attribute values.


```html
  <!-- bad -->
  <a class='main-button'>Sign in</a>

  <!-- good -->
  <a class="main-button">Sign in</a>
```

### Attribute order
HTML attributes should come in this particular order for easier reading of code.

 - class
 - id, name
 - data-*
 - src, for, type, href, value
 - title, alt
 - role, aria-*

Classes make for great reusable components, so they come first. Ids are more specific and should be used sparingly (e.g., for in-page bookmarks), so they come second.
```html
<a class="..." id="..." data-toggle="modal" href="#">
  Example link
</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```

### Meta Tags:
#### Character set
Ensure that all websites use UTF-8 character sets so that the pages can be read universally

```html
  <meta charset="utf-8">
```
#### Mobile / Responsive
Make sure to include a viewport meta tag when building a responsive or mobile dedicated website
<https://developer.mozilla.org/en-US/docs/Mobile/Viewport_meta_tag>

```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

#### IE compatibility mode
Internet Explorer supports the use of a document compatibility `<meta>` tag to specify what version of IE the page should be rendered as. Unless circumstances require otherwise, it's most useful to instruct IE to use the latest supported mode with *edge mode*.
```html
  <meta http-equiv="X-UA-Compatible" content="IE=Edge">
```

### Language attribute
From the HTML5 spec: _Authors are encouraged to specify a lang attribute on the root html element, giving the document's language. This aids speech synthesis tools to determine what pronunciations to use, translation tools to determine what rules to use, and so forth._
```html
<html lang="en-us">
  <!-- ... -->
</html>
```

### CSS and JavaScript includes
Per HTML5 spec, typically there is no need to specify a `type` when including CSS and JavaScript files as `text/css` and `text/javascript` are their respective defaults.
```html
<!-- External CSS -->
<link rel="stylesheet" href="code-guide.css">

<!-- In-document CSS -->
<style>
  /* ... */
</style>

<!-- JavaScript -->
<script src="code-guide.js"></script>
```

</ Wildebeest HTML Style Guide >
=
