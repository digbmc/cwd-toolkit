---
title:  "Formatting Text with Markdown"
category: "how-to"
permalink: /how-to/markdown/

header:
    teaser: /assets/images/header-1.jpg
    image: /assets/images/header-1.jpg  # Putting the path to an image here will add a header image.
    alt: "A person typing on a computer" # It is good practice to include an image desription as alt text.
    caption: "[Original Photo by Christin Hume on Unsplash](https://unsplash.com/@christinhumephoto)" # Put a caption for your image here. It will display in the bottom right corner of the image.
---

[Markdown](https://www.markdownguide.org/) is a markup language that you can use to add formatting elements to your text content. Here you will find a quick guide on how to add certain elements and what they look like within this site template. You can also take a look at the official [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/). 

If you're learning Markdown for the first time, it may help to view this post as it appears in your web browser alongside its Markdown file in the site directory. The file is found under _posts and is called 05_markdown.md.

## Headings and Paragraphs

Markdown lets you easily add headings to your text. The heading above is a level-2 heading (H2). If you're using this template, the highest heading level you should use in the content section of your posts is level 2 (H2). This is because, generally speaking, a webpage should have just one level-1 header (H1), and in this case the title specified in this post's front matter is used as the page's H1. It is also important to make sure you do not skip heading levels, as properly ordered headings improve accessibility and aid the function of screen readers. The use of properly ordered headings is also necessary for the site's built-in table of contents function to work.

Paragraphs are separated by a blank line. 

## Bold and Italic Text

**Bold** and *italic* text are created using aterisks. Here is the syntax you will use for each:

```markdown
**bold text** and *italicized text*
```

## Blockquotes

You can also add formatting for block quotes. Here is an example of a block quote followed by the code that creates it.
> This is the syntax for block quotes. A block quote can have multiple paragraphs.
>
> The syntax for a paragraph break in a block quote is similar to a regular paragraph break, except the "blank" line must have a greater-than sign at the beginning to indicate that it is part of the block quote.

```markdown
> This is an example of a block quote. A block quote can have multiple paragraphs.
>
> The syntax for a paragraph break in a block quote is similar to a regular paragraph break, except the "blank" line must have a greater-than sign at the beginning to indicate that it is part of the block quote.
```

## Lists

Lists come in two types: ordered and unordered.

### Ordered Lists

Ordered lists begin with numbers, and they look like this:
1. A list item
2. Another list item
3. Yet another list item

The syntax is simple. It looks like this:
```markdown
1. A list item
2. Another list item
3. Yet another list item
```

### Unordered lists.

Unordered lists begin with bullet points, and they look like this:
- A list item
- Another list item
- Yet another list item

In the code, it looks like this:
```markdown
- A list item
- Another list item
- Yet another list item
```

## Links

To add links in Markdown, enclose the visible text of the link in square brackets `[]` and the permalink or url of the link's destination in parentheses `()`. Together, it looks like this: `[linked text](url)`. Here are a few different ways you can use links in your webpages:
```markdown
{% raw %}
- This sentence links to [another website](https://github.com/digbmc/ds-project).
- This sentence contains a link to the ["Links" section of this page](#links).
- This sentence contains a link to the [Projects]({{ "/how-to/adding-content/#projects" | absolute_url }}) section on this site's [Adding Content]({{ "/how-to/adding-content/" | absolute_url }}) page.
{% endraw %}
```
And here is how each of the above sentences is rendered on the webpage:
- This sentence links to [another website](https://github.com/digbmc/ds-project).
- This sentence contains a link to the ["Links" section of this page](#links).
- This sentence contains a link to the [Projects]({{ "/how-to/adding-content/#projects" | absolute_url }}) section on this site's [Adding Content]({{ "/how-to/adding-content/" | absolute_url }}) page.

## Footnotes

You may want to include footnotes in your text content.[^1] You can add footnotes to your text using Markdown.[^2] 

Here's what the code for the above section looks like:
```markdown
You may want to include footnotes in your text content.[^1] You can add footnotes to your text using Markdown.[^2] 

[^1]: Footnotes look like this.

[^2]: 
    Footnotes can have line breaks and multiple paragraphs.
    
    When you are formatting a footnote with paragraph breaks or block quotes like this one, make sure each line of the footnote is indented by 4 spaces. Otherwise, you can use the normal syntax for paragraph breaks and block quotes.
    > Footnotes can even contain block quotes like this one.
```

Regardless of where in the code you put the text for the footnotes, they will display at the bottom of the page's content section. That said, it may help to keep all of the footnotes in one place at the end of your post's content.

[^1]: Footnotes look like this.

[^2]: 
    Footnotes can have line breaks and multiple paragraphs.

    When you are formatting a footnote with paragraph breaks or block quotes like this one, make sure each line of the footnote is indented by 4 spaces. Otherwise, you can use the normal syntax for paragraph breaks and block quotes.
    > Footnotes can even contain block quotes like this one.
