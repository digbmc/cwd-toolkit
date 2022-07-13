---
title:  "Creating files"
category: "spotlight"
permalink: /how-to/creating-files/

header:
    teaser: /assets/images/default-3.jpg
    image_description: "A close up of typewriter keys." # It is good practice to include an image desription as alt text.
    caption: "[Photo by Camille Orgel on Unsplash](https://unsplash.com/@cam_bam)" # Put a caption for your image here. It will display in the bottom right corner of the image.
---

It's great that you're here! In order to edit this webpage and make it your own, our site is set up to be controlled by files that combine two basic programming languages: YAML and Markdown. To add/edit pages or projects all you need to do is edit one of our existing markdown files or create your own. 

Keep reading to learn how to get started. 

## What are YAML and Markdown?

[Markdown](https://www.markdownguide.org/) is a plain-text markup language that makes it easy to format your text. Markdown converts what you write in words into HTML code that is readable by your computer. HTML is denoted as **.md** in your files. Because it is so useful for writing, Markdown is an integral element to creating pages, projects, and posts on this site.  


[YAML](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started) (Yet Another Markdown Language or yml) is a specific category of markdown language that “serializes” or stores data. For example, it can store data on the date, title of a post, category, and so on. One important differentiation of YAML from markdown is that YAML uses indentation-based scoping. According to [CloudBees](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started), indentation denotes a new, nested line: 

> *Whitespace is part of YAML's formatting. Unless otherwise indicated, newlines indicate the end of a field. You structure a YAML document with indentation. The indentation level can be one or more spaces. The specification forbids tabs because tools treat them differently.*

In creating webpages, YAML files are denoted by a **.yml** tag, such as in the `_config.yml` file in this site’s code which stores all the basic data for the site, such as dates, titles, categories, and authors. 

Here is an excerpt from our `_config.yml` file. It looks like this: 

```yaml
theme                  : "minimal-mistakes-jekyll"
minimal_mistakes_skin    : "academic" 

# Site Settings
locale                   : "en-US"
title                    : "Critical Web Design Toolkit"
```

As you can see, we chose to include information on the theme, skin, locale, and site title.

Also, the information in the `_config.yml` file is not coded to update regularly, so you have to restart your program to see the changes made. 

### Working together

In your code, YAML and Markdown often work together in .md files. 

They look like this:

```markdown 
---
layout: single
title:  "Images"
category: ["how-to", "spotlight"]
permalink: /how-to/images/

toc: true
toc_label: "On this page"

---

# A header title

```

Above, the YAML **front matter** is used to store data about this markdown page and communicate with the HTML and Liquid code. For example, the category section will store this page in both the "how-to" and "spotlight" categories and display them on the front page accordingly.   

In this site, we use yml front matter at the top of every markdown file. It is always characterized by `---` to enclose the yml code and placed at the very top of the file.  

## How to use front matter in .md files

To create this site, data is stored and sorted for each markdown file using yml front matter. When creating a markdown (.md) file, you should *always* include a yml header, or else the program will not understand what to do with the file.  

### Trying it yourself

To create your own .md file, you can copy and past the following code into the top of your new .md file:

```yaml
---
layout: single
title:  "Project Page Template" # Replace this with the title of your project.
tagline: "Copy the code in this file and replace the content with your own." # Add your own tagline or leave this line empty.
author: "Your Name"
category: ["templates"] # Give the post the "spotlight" category if you want it to appear in a large box on the homepage, or give it a category that matches one in _data/content.yml .
permalink: /templates/project/ # links to this page. Must be edited depending on page title.

header:
    teaser: /assets/images/default-3.jpg # The image you put here will appear as a teaser on the site's homepage.
    image: /assets/images/default-3.jpg  # Putting the path to an image here will add a header image.
    image_description: "Describe your header image here." # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image. This is a good place to give credit to the photographer or source.
    show_overlay_excerpt: true # Set this to false if you do not want a tagline or excerpt to appear in your page header.

sidebar:
    nav: "categories"
    
toc: true # toc stands for "table of contents," if turned to "true" it automatically generates a table of contents based on your markdown headings, either h1 #, h2 ##, or h3 ### 
toc_label: "On this page" # label at the top of your toc

works-cited: # Put your sources in here as a list in alphabetical order, each item should be in quotations, add italics using html tags <i></i>. The first item is an example...
    - item: "Wilde, Oscar. <i>The Picture of Dorian Grey</i>. Ward Lock & Co., 1891, https://en.wikisource.org/wiki/The_Picture_of_Dorian_Gray_(1891)."
---
# h1 heading
## h2 heading
## h3 heading

Add your markdown here. 
```

You can keep, add, or remove front matter items as you'd like, depending on your goal. For example, you can leave author blank if including author names is not a part of your project. 

To learn more about formatting text in Markdown, click onto the next page... 
