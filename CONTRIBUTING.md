---
title: Article styling guide
language: en
---

# Article styling guide

This website uses a dialect of Markdown, called [**GitHub Flavored
Markdown**][gfm] (GFM), to author pages. Below are recommendations and
guidance on the usage of Markdown.

## Basic rules

**Use empty lines to separate paragraphs.** This is a Markdown and
plain text styling convention.

**Do not start a paragraph with spaces.** Markdown engines inteprets
this as a code block, which is something you probably don't want.

<div class="example" markdown="1">

Markdown:

```markdown
A new line
does not mark paragraphs.

Two, though, does.

    If I indent the first line as in books, though,
bad things will happen.
```

Result:

<div class="result" markdown="1">

A new line
does not mark paragraphs.

Two, though, does.

    If I indent the first line as in books, though,
bad things will happen.

</div>
</div>

**Markdown should be used in place of equivalent HTML.** This improves
readability.

## Length of a line

**A line in a markdown file must not exceed 80 columns.** This is an
established tradition from the dawn of computers. This also makes the
article readable on a terminal; anything longer would be tiring to
human.

**A line in a markdown file should not exceed 72 columns.** Unlike the
80-column rule, this is more a recommendation. 72 columns is the
recommended line length for documentation, by Python standards; here,
it is extended to all Markdown files.

**Do not hyphenate text.** The website would do it automatically for
readers, and doing so manually would result in extra hyphens on the
web page, breaking user experience.

## Emphasis

**Use asterisks (`*`) to emphasize text.** To make a text italic, use
a single asterisk around the emphasized text. To make a text bold, use
two asterisks. Underlines (`_`) should not be used for emphasis.

<div class="example" markdown="1">

Markdown:

```markdown
I am an ordinary guy.
**My friend is bold**.
*Another of my friend is italic.*
```

Result:

<div class="result" markdown="1">

I am an ordinary guy. **My friend is bold**. *Another of my friend is
italic.*

</div>
</div>

## Headings

**All headings should use the ATX style.** An ATX style heading starts
with a specific number of `#` signs indicating the heading level; One
`#` sign indicates the title of an article, Two `#` signs indicates
a section title, *et cetera*. A space should follow the `#` signs,
after which the content of the heading is written. Setext style
headings should not be used, and a heading should not end with a `#`
sign.

<div class="example" markdown="1">

Markdown:

```markdown
# Title

## Section

### Subsection

#### Sub-subsection

##### Paragraph

###### Sub-paragraph
```

Result:

<div class="result" markdown="1">

# Title

## Section

### Subsection

#### Sub-subsection

##### Paragraph

###### Sub-paragraph

</div>
</div>

**Level 1 headings should only be used once at the top of an article.**
A level 1 headings indicates the title of an article. For section
headings, use level 2 headings instead.

## Code

To embed code in a paragraph, wrap the code with a pair of backticks
(`` ` ``).

<div class="example" markdown="1">

Markdown:

```markdown
This paragraph contains `embedded` code.
```

Result:

<div class="result" markdown="1">

This paragraph contains `embedded` code.

</div>
</div>

To create a code paragraph, use three backticks (```` ``` ````).

<div class="example" markdown="1">

Markdown:

````markdown
```
This is a block of code.
```
````

Result:

<div class="result" markdown="1">

```
This is a block of code.
```

</div>
</div>

To specify the language of a code paragraph, put the language name
directly after the opening backticks.

<div class="example" markdown="1">

Markdown:

````markdown
```c
#include <stdio.h>

int main()
{
    /* Hello world program in C */
    printf("Hello, world");
    return 0;
}
```
````

Result:

<div class="result" markdown="1">

```c
#include <stdio.h>

int main()
{
    /* Hello world program in C */
    printf("Hello, world");
    return 0;
}
```

</div>
</div>

## Block quotes

Use `>` to quote text.

<div class="example" markdown="1">

Markdown:

```markdown
> The course of true love never did run smooth.
```

Result:

<div class="result" markdown="1">

> The course of true love never did run smooth.

</div>
</div>

**When quoting, every line of the quoted paragraph should start with
`>`.** This ensures consistency when the source code is read.

<div class="example" markdown="1">

Markdown:

```markdown
> From fairest creatures we desire increase,
> That thereby beauty's rose might never die,
> But as the riper should by time decease,
> His tender heir might bear his memory;
> But thou, contracted to thine own bright eyes,
> Feed'st thy light's flame with self-substantial fuel,
> Making a famine where abundance lies,
> Thyself thy foe, to thy sweet self too cruel.
> Thou, that art now the world's fresh ornament
> And only herald to the gaudy spring,
> Within thine own bud buriest thy content
> And, tender churl, mak'st waste in niggarding.
> Pity the world, or else this glutton be,
> To eat the world's due, by the grave and thee.
```

Result:

<div class="result" markdown="1">

> From fairest creatures we desire increase,
> That thereby beauty's rose might never die,
> But as the riper should by time decease,
> His tender heir might bear his memory;
> But thou, contracted to thine own bright eyes,
> Feed'st thy light's flame with self-substantial fuel,
> Making a famine where abundance lies,
> Thyself thy foe, to thy sweet self too cruel.
> Thou, that art now the world's fresh ornament
> And only herald to the gaudy spring,
> Within thine own bud buriest thy content
> And, tender churl, mak'st waste in niggarding.
> Pity the world, or else this glutton be,
> To eat the world's due, by the grave and thee.

</div>
</div>

## Other blocks

Other blocks are defined in the page styles. To use other blocks,
put a `<div>` tag with the appropriate class around the text.

**All `<div>` and `</div>` tags should be in their own paragraphs.**
This allows Markdown between them to be parsed by a CommonMark
compliant Markdown implementation.

**All `<div>` tags should carry the `markdown="1"` attribute,** to
improve compatibility with various code highlighters.

<div class="example" markdown="1">

Markdown:

```markdown
<div class="note" markdown="1">

This is a note *with some emphasized text*.

</div>

<div class="note">

There is no Markdown in this div.

</div>

<div class="note">
Nor this one.
</div>
```

Result:

<div class="result" markdown="1">

<div class="note" markdown="1">

This is a note with some *emphasized* text.

</div>

<div class="note">

There is no Markdown in this note.

</div>

<div class="note">
Nor this one.
</div>

</div>
</div>

**Inline CSS must not be used.** Inline CSS makes the text cluttered
for plain text readers, and can easily result in poor accessibility.
Even in cases that it would not harm accessibility, it would eventually
break in the event of a sitewide layout change.

In almost all cases when you want to use inline CSS, there is an HTML
element or CSS class that would suit your needs. Use them instead.

<div class="example" markdown="1">

Markdown:

```markdown
<span style="color: white;">Light color on light
color is universally hated.</span>
```

Result:

<div class="result" markdown="1">

<span style="color: white;">Light color on light
color is universally hated.</span>

</div>
</div>

Here follows the custom classes defined by this theme.

### Notes

Using the classes `note`, `example` and `warning` creates blocks that
respectively indicate a note on previous content, an example, and a
warning.

<div class="example" markdown="1">

Markdown:

```markdown
<div class="note" markdown="1">

This is a note.

</div>

<div class="example" markdown="1">

This is an example.

</div>

<div class="warning" markdown="1">

Watch out for bugs.

</div>
```

Result:

<div class="result" markdown="1">

<div class="note" markdown="1">

This is a note.

</div>

<div class="example" markdown="1">

This is an example.

</div>

<div class="warning" markdown="1">

Watch out for bugs.

</div>

</div>
</div>

[gfm]: https://github.github.com/gfm/
