---
title: Skip link
---

Skip links provide ways for assistive technology users to skip directly to pertinent content. Instead of having to tab through an entire navigation, users can use a skip link, often the first link placed on a page for such users, to skip directly to the content that you want them to see. 

Here's an example of a skip link:

``` html

  <body>
    <a id='skip-nav' class='screenreader-text' href='#main-content'>
      Skip Navigation or Skip to Content
    </a>

    <main id='main-content'>
      …Content here…
    </main>

  </body>

```

A few important points about the skip link example:

* The skip link is the first element inside of the `<body>` tag, which would make it the first element that a user would 'select' when hitting tab.
* Not shown, but important - It is best practice to 'hide' the skip link from sighted users, but 'show' it to users of assistive technology. This can be achieved with CSS.
* The skip link should include descriptive text as to what it will do when clicked.

To 'hide' the link, use some CSS like this (feel free to change class names or other attributes as suitable for your project):

```css
.screenreader-text {
  position: absolute;
  left: -999px;
  width: 1px;
  height: 1px;
  top: auto;
}
.screenreader-text:focus {
  color: black;
  display: inline-block;
  height: auto;
  width: auto;
  position: static;
  margin: auto;
}

```

## Further Reading

- [a11yproject - Use skip navigation links
](https://www.a11yproject.com/posts/2013-05-11-skip-nav-links/)

## Examples of Skip Links

- [starbucks.com](https://www.starbucks.com/)
- [csstricks.com](https://css-tricks.com/)
