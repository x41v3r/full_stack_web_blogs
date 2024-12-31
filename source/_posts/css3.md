---
title: CSS3
date: 2024-12-30 16:02:43
tags:
---

# 1 Getting started with CSS

## 1.1 What is CSS?

&emsp;&emsp;CSS (Cascading Style Sheets) is used to style and lay out web pages.

## 1.2 Adding CSS to the document

There are three different ways to apply CSS to an HTML document.

### External stylesheets

```css
/*styles.css*/
h1 {
    color: red;
}
```

To link styles.css to index.html, add the following line somewhere inside the `<head>` of the HTML document:

```html
<link rel="stylesheet" href="styles.css" />
```

### Internal stylesheets

Internal stylesheets are contained within `<style>` elements, which go inside the HTML `<head>`.

```html
<style>
    p {
        color: purple;
    }
</style>
```

### Inline styles

Inline styles are CSS declarations that *affect a single HTML element*, contained within a style attribute.

Add a `style` attribute to the element to specify its style.

```html
<span style="color: purple; font-weight: bold">span element</span>
```

> **Avoid using CSS in this way if possible.** It is a bad practice.

## 1.3 Selectors

### 1.3.1 What is a selector?

A CSS selector is a pattern of elements and other terms that tell the browser *which HTML elements should be selected to have the CSS property values inside the rule applied to them*.

The element or elements which are selected by the selector are referred to as the subject of the selector.

### 1.3.2 Type selectors



## 1.4 Combinators

## 1.5 The box model

# 2 Text styling

# 3 Layout

