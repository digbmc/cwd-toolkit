---
title:  "Bibliography"
category: "how-to"
permalink: /how-to/bibliography/

header:
    teaser: /assets/images/default-4.jpg
    image: /assets/images/default-4.jpg  # Putting the path to an image here will replace the header image.
    alt: "Books on an ornate wooden bookshelf." # It is good practice to include an image desription as alt text.
    caption: "[Photo by Mario Klassen on Unsplash](https://unsplash.com/@marioklassen)" # Put a caption for your image here. It will display in the bottom right corner of the image.

works-cited: # Put your sources in here as a list in alphabetical order, each item should be in quotations, add italics using html tags <i></i>
    - item: "Stoker, Bram. <i>Dracula</i>. Project Gutenberg, 1897, https://www.gutenberg.org/ebooks/345."
    - item: "Wilde, Oscar. <i>The Picture of Dorian Grey</i>. Ward Lock & Co., 1891, https://en.wikisource.org/wiki/The_Picture_of_Dorian_Gray_(1891)."
---

This post shows how to add a bibliography to your projects.

## Adding Works Cited to the YAML Front Matter
If you want to add a bibliography to your project, add the following code to the project's YAML front matter and edit the list of items to contain the works you intend to cite. 
```
works-cited: # Put your sources in here as a list in alphabetical order, each item should be in quotations, add italics using html tags <i></i>
    - item: "Stoker, Bram. <i>Dracula</i>. Project Gutenberg, 1897, https://www.gutenberg.org/ebooks/345."
    - item: "Wilde, Oscar. <i>The Picture of Dorian Grey</i>. Ward Lock & Co., 1891, https://en.wikisource.org/wiki/The_Picture_of_Dorian_Gray_(1891)."
```

## Adding Citations to Your Text

To give examples of how different citations look and function, this page includes quotes from books that are in the public domain, such as this one from *Dracula*: "It is really wonderful how much resilience there is in human nature."[^1] If you're using the Chicago citation format, you can format citations as footnotes like the one preceding this sentence, or if you are using MLA or APA format, you could use parenthetical citation, like this [(Stoker)](#bibliography). Footnote citations use the standard Markdown syntax for footnotes, which looks like this:
```markdown
To give examples of how different citations look and function, 
this page includes quotes from books that are in the public domain, 
such as this one from *Dracula*: "It is really wonderful how much 
resilience there is in human nature."[^1]

## Notes

[^1]: Stoker, https://www.gutenberg.org/ebooks/345.
```

And parenthetical citations that link to the Bibliography section of the page use the Markdown syntax for links, which looks like this:
```markdown
If you are using MLA or APA format, you could use parenthetical citation, like this [(Stoker)](#bibliography).
```
You can also choose to not link your parenthetical citations to the Bibliography section. In that case, no special Markdown syntax is necessary.

You can also add citations to blockquotes. Here is an example of a blockquote with a footnote citation:

> "They say that when good Americans die they go to Paris," chuckled Sir Thomas, who had a large wardrobe of Humour's cast-off clothes.
> 
> "Really! And where do bad Americans go to when they die?" inquired the duchess.
> 
> "They go to America," murmured Lord Henry. [^2]

NOTE: If you intend to use both footnotes and a bibliography on a post, it is recommended to end the post with a level-2 header called "Notes," like the one below, and list your footnotes beneath it.

## Notes

[^1]: Stoker, https://www.gutenberg.org/ebooks/345.
[^2]: Wilde, https://en.wikisource.org/wiki/The_Picture_of_Dorian_Gray_(1891).