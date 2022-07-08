---
layout: single
title:  "This is a post with a bibliography"
category: ["how-to"]
permalink: /how-to/bibliography/

header:
    teaser: /assets/images/default-4.jpg
    overlay_image: /assets/images/default-4.jpg  # Putting the path to an image here will replace the header image.
    image_description: "Describe your image here" # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image.

sidebar:
    nav: "categories"

toc: true;
toc_label: "On this page"

works-cited: # Put your sources in here as a list in alphabetical order, each item should be in quotations, add italics using html tags <i></i>
    - item: "Stoker, Bram. <i>Dracula</i> .Project Gutenberg, 1897, https://www.gutenberg.org/ebooks/345."
    - item: "Wilde, Oscar. <i>The Picture of Dorian Grey</i>. Ward Lock & Co., 1891, https://en.wikisource.org/wiki/The_Picture_of_Dorian_Gray_(1891)."
---

This post shows how to add a bibliography to your projects.

## Adding Works Cited to the YAML Front Matter
If you want to add a bibliography to your project, add the following code to the project's YAML front matter and edit the list of items to contain the works you intend to cite. 
```
works-cited: # Put your sources in here as a list in alphabetical order, each item should be in quotations, add italics using html tags <i></i>
    - item: "Stoker, Bram. <i>Dracula</i> .Project Gutenberg, 1897, https://www.gutenberg.org/ebooks/345."
    - item: "Wilde, Oscar. <i>The Picture of Dorian Grey</i>. Ward Lock & Co., 1891, https://en.wikisource.org/wiki/The_Picture_of_Dorian_Gray_(1891)."
```
To give examples of how different citations look and function, this page includes quotes from books that are in the public domain, such as this one from *Dracula*: "It is really wonderful how much resilience there is in human nature."[^1] You can format citations as footnotes like the one preceding this sentence, or you could use parenthetical citation, like this [(Stoker)](#bibliography).
## Adding Citations to Your Text

(Write about how to add citations to text)

Example blockquote with footnote citation:

> "They say that when good Americans die they go to Paris," chuckled Sir Thomas, who had a large wardrobe of Humour's cast-off clothes.
> 
> "Really! And where do bad Americans go to when they die?" inquired the duchess.
> 
> "They go to America," murmured Lord Henry. [^2]


This section is being used to experiment with the use of both footnotes and a bibliography. Here is a sentence from *The Picture of Dorian Grey*: "But he never fell into the error of arresting his intellectual development by any formal acceptance of creed or system, or of mistaking, for a house in which to live, an inn that is but suitable for the sojourn of a night, or for a few hours of a night in which there are no stars and the moon is in travail." [^3]

If you intend to use both footnotes and a bibliography on a post, I recommend ending the post with a level-2 header called "Notes," like the one below.

## Notes

[^1]: Stoker
[^2]: Wilde
[^3]: Wilde