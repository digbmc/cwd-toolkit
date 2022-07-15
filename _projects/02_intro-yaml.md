---
title:  "Adding and Editing Content"
category: "spotlight"
permalink: /how-to/adding-content/

header:
    teaser: /assets/images/default-3.jpg
    alt: "A close up of typewriter keys." # It is good practice to include an image desription as alt text.
    caption: "[Photo by Camille Orgel on Unsplash](https://unsplash.com/@cam_bam)" # Put a caption for your image here. It will display in the bottom right corner of the image.
---

In order to add and edit the content of your site, you will create and make changes to a number of Markdown files. These are files that end in the file extension .md, and they include index.md file as well as all of the files in _pages and _projects. Each of these files has two main sections: the front matter, which is written in YAML, and the content, which is written using Markdown. You can also include some HTML in these files, as Jekyll will convert them to HTML anyway when it builds the site.

## What are YAML, Markdown, and HTML?

### YAML

[YAML](https://yaml.org/) (YAML Ain't Markup Language) is a human-readble data serialization language that can store data that tells Jekyll how to build your site. For example, it can be used to set the title, layout, and permalink of a page on your site. It is important to note that YAML uses indentation-based scoping. According to [CloudBees](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started), indentation denotes a new, nested line: 

> *Whitespace is part of YAML's formatting. Unless otherwise indicated, newlines indicate the end of a field. You structure a YAML document with indentation. The indentation level can be one or more spaces. The specification forbids tabs because tools treat them differently.*

In addition to Markdown files, which contain your site's content, your site also has YAML files, which are denoted by a **.yml** file extension. One such file is the `_config.yml` file, which stores the configuration information that tells Jekyll how to build your site. 

### Markdown

[Markdown](https://www.markdownguide.org/) is a plain-text markup language that makes it easy to format your text. Markdown converts what you write in words into HTML code that web browsers can read. Because it is so useful for writing, Markdown is an integral element to creating pages, projects, and posts on this site. This template has a guide on [Formatting Text with Markdown]({{ "/how-to/markdown/" | absolute_url }}), which you can check out later.

### HTML

You do not need to know the ins and outs of HTML to use this site template, but it can help you edit some of the template's basic formats. Other articles in the How-To section of the template will show you how to do some things with HTML, like adding embedded content. If you want more information on HTML, check out the [W3 Schools resources on HTML](https://www.w3schools.com/html/).

## Editing the Homepage

You may use YAML, Markdown, and HTML together in your pages and projects. Let's take a look at the default index.md file, which Jekyll uses to build the site's homepages.
```markdown
---
layout: home
title: {{ site.title }}
author_profile: false # Setting this to true will display the site author information specified in _config.yml in this page's left sidebar.

header:
    image: /assets/images/home.jpg  # Putting the path to an image here will add that image to this page's header.
    alt: "A large library with tall bookshelves and marble busts." # Describe the header image here
    caption: "[Photo by Alex Block on Unsplash](https://unsplash.com/@alexblock)" # Add a visible caption to your image or give credit to the photographer or source.

sidebar:
    nav: "categories"

include_categories:   
  - how-to
  - templates

classes: wide # Setting the class as wide will extend the page's content into the right margin.
---

You can replace the text in this section with your own text such as an introduction to your site.

Below you will find instructions on how to install and configure your site as well as how to add and format your own content. You can safely delete them from your repository if you are done referencing them.

{% comment %} "Spotlight" projects display as boxes that take up the full width of this content section. They are ideal for highlighting your website's most important projects or if you do not have so many projects that a gallery view would be necessary. Add projects to this section by giving them the 'spotlight' category. {% endcomment %}
<div class="spotlight"> 
{% assign spotlight_projects = site.projects | where: 'category', 'spotlight' %}
{% include spotlight projects = spotlight_projects %}
</div>

{% comment %} The "collection_row" section displays a gallery of projects organized by category. You must specify which categories you would like to be displayed on your homepage in the front matter of this file under "include_categories", and the code below will loop through all of the projects, find the posts in each of the specified "include_categories", and display them in corresponding sections. {% endcomment %}
{% for c in page.include_categories %}
<div id="{{ c }}" class="pane">
<h3>{{ site.data.content.display_categories[c] }}</h3>
{% assign category_projects = site.projects | where: 'category', c  %}
{% include collection_row projects = category_projects %} 
</div>
{% endfor %}

```

Above, the YAML **front matter**, which is enclosed by triple dashes like this `---`, is used to store data about this Markdown file that tells Jekyll how to build it into the site. YAML front matter must be at the top of every Markdown file that you want to be built into your site, otherwise Jekyll will ignore it. 

The section after the enclosed YAML front matter is the file's content section, and the text content in it is written in Markdown (the text at the top of the section that looks like plain, readable text), but you will notice that this section also contains some Liquid (in the curly brackets) and some HTML. This code adds some unique features to the homepage that Markdown itself cannot support. The Markdown text at the top of the section can be safely edited, but the Liquid and HTML code at the bottom should not be changed.

## Creating Your Own Pages and Projects

About the difference of pages and projects

### Pages

About editing and creating pages

### Projects

A good way to start making your own projects is to copy the code of the project template. First, though, you should create a file in the _projects section and name it with the following format: 00_filename.md, where you can replace 'filename' with whatever name you choose. The two-digit number at the beginning of the filename will determine the order in which the "previous" and "next" buttons at the bottom of each project will navigate through the projects.


