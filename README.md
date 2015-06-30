# < Wildebeest HTML Style Guide >

*A mostly reasonable approach to HTML*


## <a name='TOC'>Table of Contents</a>
**(Work in progress...)**

### HTML quotation marks
When quoting attributes values, use double quotation marks. Use double ("") rather than single quotation marks ('') around attribute values.


```html
  <!-- bad -->
  <a class='main-button'>Sign in</a>

  <!-- good -->
  <a class="main-button">Sign in</a>
```

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

### Doc Type:
Ensure that all websites use the new HTML5 doctype

```html
<!DOCTYPE html>
```

### alt attribute:
All images which are using the <img> tag should use the alt attribute. If not alternative is provided, it is still mandatory to use the alt attribute but with an empty string to comply with accessibility rules.

```html
  <img src="smiley.jpg" alt="Smiley face" />
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

</>
=
