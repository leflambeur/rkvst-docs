---
title: "Style Guide"
description: ""
lead: ""
date: 2021-05-20T19:23:22+01:00
lastmod: 2021-05-20T19:23:22+01:00
draft: false
images: []
menu: 
  contributing:
    parent: "formatting-content"
weight: 8
toc: true
---

Doks uses Goldmark markdown which is primarily Github-flavoured

Here are some examples of how to use it that meet our [Style Guide](style-guide) 

## Headings

Headings in markdown can be added using the `#` character

The more `#` you use the smaller the heading will be

```markdown
# Example Header 1
## Example Header 2
### Example Header 3
```

This would render as:

# Example Header 1
## Example Header 2
### Example Header 3

> 💡 We do not allow `# Header 1` sizing, this should only be added by the title of the article
> use `## Header 2` sizing and below for in-article headers

All headers in an article can be permalinked to easily share a specific topic quickly

## Emphasis

Markdown allows you to add emphasis to text in line using either `*` or `_` at both ends of some text

Emphasis includes Bolding and Italicizing but ***not*** Underlining

```markdown
*This is italicized*
**This is bolded**
***This is both italicized and bolded***
```

*This is italicized*</br>
**This is bolded**</br>
***This is both italicized and bolded***</br>

## Creating Lists

You can create both ordered lists and unordered lists with markdown

### Ordered Lists

Ordered lists can be created either using the specific numbers or just a single number

```markdown
1. This is 
1. An Example
1. Of an Ordered List
```
1. This is 
1. An Example
1. Of an Ordered List

### Unordered Lists

Unordered Lists can be created using `*` at the beginning of a line

```markdown
* This is
* An Example
* Of an Unordered List
```

* This is
* An Example
* Of an Unordered List

### Sub-Items in a List

You can also make sub-items in either ordered or unordered lists by indenting by a tab (or 4 spaces)

```markdown
* This is
* An Example
  * Of sub items
    * And how to format them
* In an Unordered List
```

* This is
* An Example
  * Of sub items
    * And how to format them
* In an Unordered List