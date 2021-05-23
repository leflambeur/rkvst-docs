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

It is important in any documentation to have a readable, sane and consistent experience, to that end we have defined some guidelines to ensure all content meets the same standard.

## Headings

When seperating Articles into Topics and Subsections it is preferred to use Headings as a delimiter instead of alternatives like Horizontal Rules.

Markdown does support different formats for defining Headers including underlining text with either `=` or `-`; as those formats only apply to `#Header 1` and `Header 2` respectively, for consistency across all Header sizes we have opted to use `#` instead.

The top level header ( `# Header 1`) is defined in the Article's metadata, so it is necessary to only use `## Header 2` or below.

It is also preferable to only use either `## Header 2` for Topics or `### Header 3` for Subsections of a Topic, while smaller sizes are permitted they do not render in the right-hand overview so should be used sparingly.

We observe the [Markdown Guide Best Practice](https://www.markdownguide.org/basic-syntax/#heading-best-practices) of leaving a space after the `#`.

We follow [Chicago Manual of Style](https://en.wikipedia.org/wiki/Title_case) Capitalization rules for Headings:

* Always capitalize the first and last words of titles and subtitles.
* Always capitalize "major" words (nouns, pronouns, verbs, adjectives, adverbs, and some conjunctions).
* Lowercase the conjunctions and, but, for, or, and nor.
* Lowercase the articles the, a, and an.
* Lowercase prepositions, regardless of length, except when they are stressed, are used adverbially or adjectivally, or are used as conjunctions.
* Lowercase the words to and as.
* Lowercase the second part of Latin species names.


```md
## Example Header 2
### Example Header 3
```

## Body

Content is written in place and without any special tagging or formatting.

### Grammar

We do expect standard English Grammar, this includes full use of appropriate punctuation; however Emphasis using Exclamation Marks `!` should be minimized where possible.

It is relevant to note that the authors of this documentation are primarily native British English speakers, however, there is a conscious effort to align to certain standards observed in most other technical documentation including Americanized Spellings for consistency.

This includes:
* Use of the Oxford Comma
* Use of 'z' instead of 's' in words like 'Organization'
* Use of the '-or' suffix instead of '-our' in words like 'Color' and 'Humor' 

We expect any contributors to also match these standards.

### Sentences

One-liner Sentences are preferable to paragraphs where possible and should be seperated by newlines in a semi-bullet standard.

Sentences should preferably be between 1-2 clauses where possible, using 3 clauses is permitted but should be minimized.

One-Liner Sentences are useful when describing how to do something, including making simple instructions.

```md
This is a sentence.

This is another sentence, this one does use commas though.
```

### Paragraphs

Pargraphs consist of 2 or more sentences and are better suited to creating conceptual narratives.

In order to not overwhelm users they should be kept to a minimum and only used for expository reasons such as describing a specific concept or topic in more detail than a single sentence would permit.

```md
This is a paragraph which demonstrates the value of narratives 
in documentation. This is because certain concepts can only 
be related with more complex grammatical structures demonstrating 
not only the concept in mind, but other key related features; 
not to mention the greater range of expression.
```

### Quotes

Quotes should use single quote marks `'` instead of Speech Marks `"`.

'This is a Quote'

Single Quotes are permitted when referring to a colloquial or adopted term such as 'Code Fences' that is not a code reference but you may wish to highlight.

If a nested quote is being used then you may use `"`.

'Of course, he said "Let's write out an example".'

### Emphasis

Emphasis should be used minimally but can be effective to highlight key words and phrases inside of a sentence that need specific attention.

In most scenarios it is preferable to use a [callout]() instead.

Use of Emphasis to highlight words differs to the usage of inline code references.

Emphasis should be used when it is important to note a specific adjective/adverb or a specific noun.

While it is permitted to emphasize an entire sentence this should only be done for stylistic purposes and emphasis should be kept to single words or small phrases.

When used in the context of an adjective/adverb use both Italics and Bold adding three asterisks `***` at either end of the highlighted text.

When used in the context of a noun use only Bold adding two asterisks `**` at either end of the highlighted text.

We do not permit use of underscored `_` emphasis, only asterisks`*` will be accepted.

For example:

```md
This action is available ***only*** to **Root Users**. 
```

This action is available ***only*** to **Root Users**.

### Linebreaks

Inserting manual linebreaks is not usually necessary to include as Markdown is very effective at rendering most scenarios.

However in a situation where the rendering is not working it is permitted to use standard linebreaks `<br>` in order to fix both formatting and style.

## Lists

We support both ordered and unordered lists in markdown.

### Ordered Lists

Ordered lists should be written using the full numerical standard.

This means that while it is possible to list items only using one number and it will be rendered correctly we will only permit fully complete numbering to be submitted.

We also only permit using periods `.` as delimiters as this is a more standardized pattern than parentheses `)`.

```md
1. This is
2. an Ordered
3. List
```

1. This is
2. an Ordered
3. List

### Unordered Lists

Unordered Lists should be written using only asterisks `*` at the beginning of a line of text.

Other unordered list styles including `+` and `-` are available in markdown but are not permitted in these Docs.

```md
* This is
* an Unordered
* List
  * Unordered Lists
  * Can have sub-items
```

* This is
* an Unordered
* List
  * Unordered Lists
  * Can have sub-items

## Code and Codeblocks

There are many ways to use Inline Code and Codeblock references within the Jitsuin Docs.

### Inline Code

Inline code is specified using backticks `` ` ``, it is preferable to label any code, object attributes or other API references using inline code to highlight.

For example:

```md
note we have included the values `arc_display_name`, `arc_description` and `arc_home_location_identity`
```

note we have included the values `arc_display_name`, `arc_description` and `arc_home_location_identity`

### Standard Codeblocks

Standard codeblocks are represented using markdown with three backticks `` ``` `` as 'code fences'.

The Docs have built in syntax highlighting using `highlight.js` which allows us to add a language to each codeblock for proper rendering in the following format:

<pre><code>
```bash
```
</pre></code>

Here is an example of the full Syntax Highlighting:

```bash
#!/bin/bash

###### CONFIG
ACCEPTED_HOSTS="/root/.hag_accepted.conf"
BE_VERBOSE=false

if [ "$UID" -ne 0 ]
then
 echo "Superuser rights required"
 exit 2
fi

genApacheConf(){
 echo -e "# Host ${HOME_DIR}$1/$2 :"
}

echo '"quoted"' | tr -d \" > text.txt
```

There is a list of Languages available in the [Advanced Formatting Section](../advanced-formatting/).

It is required that each codeblock has a language associated with it, if in doubt a standard default to use is the markdown syntax (`md`).

It is preferable that Standard Codeblocks are used for representing shell commands and API Responses in documentation where there is typically little variance across platforms, and not scripting examples which should use Tabbed Codeblocks instead.

### Shell Commands

Commands should use Standard Codeblocks with the `bash` syntax highlight, we don't permit adding a leading command prompt such as `#` or `$`.

<pre><code>
```bash
echo "this is a command"
```
</code></pre>

```bash
echo "this is a command"
```

### Tabbed Codeblocks

Where possible when writing code examples you should use Tabbed Codeblocks to offer examples in multiple languages that other users may prefer.

This creates a much more accessible and useful documentation platform for any and all users.

Where possible the following languages should be offered as examples in this order:

* `json` - a raw JSON Example of the data being submitted
* `bash` - curl implementation of interacting with the endpoint
* `python` - python implementation of interacting with the endpoint
* `go` -  go implementation of interacting with the endpoint

As Jitsuin RKVST is primarily an API there are different requirements for each type of request:

{{< tabs name="tabbed_api_requirements" >}}
{{< tab name="GET" codelang="md" >}}
Minimum:
* bash

Preferably:
* bash
* python
* go
{{< /tab >}}
{{< tab name="POST" codelang="md" >}}
Minimum:
* json
* bash

Preferably:
* json
* bash
* python
* go
{{< /tab >}}}
{{< tab name="PUT" codelang="md" >}}
Minimum:
* json
* bash

Preferably:
* json
* bash
* python
* go
{{< /tab >}}}
{{< tab name="PATCH" codelang="md" >}}
Minimum:
* json
* bash

Preferably:
* json
* bash
* python
* go
{{< /tab >}}}
{{< tab name="DELETE" codelang="md" >}}
Minimum:
* bash

Preferably:
* bash
* python
* go
{{< /tab >}}}
{{< /tabs >}}

## Callouts and Blockquotes

### Notes

### Cautions

### Warnings

### Blockquotes

## Links

### Section References

### External Links

## Images

### Standard Images

### Light Mode and Dark Mode Images

