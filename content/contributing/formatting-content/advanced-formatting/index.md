---
title: "Advanced Formatting"
description: ""
lead: ""
date: 2021-05-20T19:23:22+01:00
lastmod: 2021-05-20T19:23:22+01:00
draft: false
images: []
menu: 
  contributing:
    parent: "formatting-content"
weight: 5
toc: true
---

As Doks is based on Hugo it has many more extensible formatting options, including some custom tools we have added ourselves to enhance the delivery of documentation overall

The examples below follow our [Style Guide](../style-guide)

## Code and Codeblocks

There are three different ways to present code and references in Jitsuin Doks

### Inline Code

When talking about a single word, line of code or attribute in a whole sentence you can use single backticks (`` ` ``) to highlight the specific word or phrase

```md
This is a`single phrase` being highlighted
```

This is a `single phrase` being highlighted

If you wish to escape 1 or more backticks in inline code use double backticks ``` `` ```

```md
`` This is `an example` that uses backticks ``
```

`` This is `an example` that uses backticks ``

### Syntax Highlighting

Syntax highlighting is built into codeblocks when a language is specified, as such there should ***always*** be a language specified against at the beginning of any codeblock

Supported Languages:

* `javascript`
* `json`
* `bash`
* `html`
* `ini`
* `toml`
* `yaml`
* `md` (markdown)
* `go`
* `python`

### Simple Codeblock

If you want to add a simple codeblock for a specific example, say it is a single bash command or some example markdown you can use three backticks `` ``` `` as a fence around the block

<pre><code>
```md
This is markdown
```
</code></pre>


```md
This is markdown
```

And with Bash
<pre><code>
```bash
$ echo "This is a Bash Example"
```
</code></pre>

```bash
$ echo "This is a Bash Example"
```

### Tabbed Codeblock

Tabbed Codeblocks are not built into either Doks or Markdown, we instead use a customised HTML template that can perform the same function using Hugo Shortcodes

Each `Tabs` object on a page should have a unique identifier, you should also specify the language syntax highlighting to use per tab, this should be reflected in the title of the tab where appropriate

```go
{{</* tabs name="tab_with_code" >}}
{{{< tab name="Bash" codelang="bash" >}}
echo "This is a Bash Example."
{{< /tab >}}
{{< tab name="Go" codelang="go" >}}
println "This is a Go Example."
{{< /tab >}}}
{{< /tabs */>}}
```

{{< tabs name="tab_with_code" >}}
{{{< tab name="Bash" codelang="bash" >}}
echo "This is a Bash Example."
{{< /tab >}}
{{< tab name="Go" codelang="go" >}}
println "This is a Go Example."
{{< /tab >}}}
{{< /tabs >}}


## Callouts and Blocked Quotes

Sometimes when writing documentation it is necessary to add notes, warnings and other callouts in order to highlight specific information, we have added some custom callouts using Hugo Shortcodes

### Notes

To add a note use the following syntax, notes are always highlighted by a left ***purple*** border

```go
{{</* note >}}
This is a note
{{< /note */>}}
```


{{< note >}}
This is a note
{{< /note >}}

### Cautions

To add a caution use the following syntax, cautions are always highlighted by a left ***yellow*** border

```go
{{</* caution >}}
This is a caution
{{< /caution */>}}
```

{{< caution >}}
This is a caution
{{< /caution >}}

### Warnings

To add a warning use the following syntax, warnings are always highlighted by a left ***red*** border

```go
{{</* warning >}}
This is a warning
{{< /warning */>}}
```

{{< warning >}}
This is a warning
{{< /warning >}}

### Block Quotes

All notes, cautions and warnings use blockquote templates and classes underneath

Block Quotes are useful syntax to not only represent multiline quotes in markdown but also to create localised sections of content differentiated from code

A key feature of Block Quotes is that they implement word-wrap so even if you seperate a quote by using a newline it won't render as such

```md
>This is
>a quote
```

>This is
>a quote

Alternatively

```md
>This is a very very very long, almost way too long, I would say incredibly long
>multiline quote
```

>This is a very very very long, almost way too long, I would say incredibly long
>multiline quote

Block Quotes do respect some Markdown Syntax though which means you can implement artificial linebreaks using `<br>`

```md
>This is<br>
>a quote
```
>This is<br>
>a quote

## Tables

Tables are useful for demonstrating a range of information, they can also be rendered in most markdown flavours using ascii denominations

Rendering Markup Tables can be difficult, you may wish to make use of an online tool like [Markdown Table Generator](https://www.tablesgenerator.com/markdown_tables) to help

```md
|  Column 1 | Column 2  |
|-----------|-----------|
|  Cell 1   | Cell 2    |
```

|  Column 1 | Column 2  |
|-----------|-----------|
|  Cell 1   | Cell 2    |

## Images

A big part of any documentation is including screenshots of workflows, architecture diagrams and infographics to help illustrate a point more clearly

Image formatting and sizing can also be very difficult to get consistently right, luckily Doks has some built-in image shortcodes to help format things properly

Your image should be saved to the same directory as the article's index.md to use the following examples when adding a screenshot or picture:

```go
{{</* img src="Jitsuin_Logo_RGB_Spot.png" alt="Rectangle" caption="<em>Jitsuin Logo Example</em>" class="border-0" */>}}
```

{{< img src="Jitsuin_Logo_RGB_Spot.png" alt="Rectangle" caption="<em>Jitsuin Logo Example</em>" class="border-0" >}}

### Light Mode and Dark Mode Images

For readability it may be necessary to have two images, one that suits light mode and another dark mode, so that when the mode is toggled it renders correctly

We have added some customised shortcode that allows you to specify two individual images

The behaviour matches the original image shortcode but adds an extra `srcDrk` variable which refers to the Dark Mode image you wish to add 

```go
{{</* imgDark src="Jitsuin_Logo_RGB.png" srcDrk="Jitsuin_WhtType_RGB.png" alt="Rectangle" caption="<em>Jitsuin Dark Mode Logo Example</em>" class="border-0" */>}}
```

{{< imgDark src="Jitsuin_Logo_RGB.png" srcDrk="Jitsuin_WhtType_RGB.png" alt="Rectangle" caption="<em>Jitsuin Dark Mode Logo Example</em>" class="border-0" >}}