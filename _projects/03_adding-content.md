---
title:  "3) Adding and Editing Content"
category: "spotlight"
permalink: /how-to/adding-content/

header:
    teaser: /assets/images/ocean-teaser-3.jpg 
    image:  # Putting the path to an image here will replace the header image.
    alt: "Dark ocean waves." # It is good practice to include an image desription as alt text.
    caption: "[Original Photo by Isai Ramos on Unsplash](https://unsplash.com/@isai21)" # Put a caption for your image here. It will display in the bottom right corner of the image.
---

In order to add and edit the content of your site, you will create and make changes to a number of files called **Markdown files**. These are files that end in the file extension `.md`, and they include `index.md` file as well as all of the files in `_pages` and `_projects`. 

Each of these files has two main sections: 
1. **Front matter**, which is written in a simple coding language called YAML
2. **Content**, which is written using Markdown. You can also include some HTML in these files, as Jekyll, our site builder, will convert them to HTML anyway when it builds the site.

## What are HTML, Markdown, and YAML?

HTML, Markdown and YAML are easy-to-read programming languages used to create websites. While you don't need to know the exact definitions of these three programming languages, it is helpful to understand a little bit about what they do in order to help you build your site.  

### HTML

You do not need to know the ins and outs of HTML to use this site template, but it can help you edit some of the template's basic formats. Other articles in the How-To section of the template will show you how to do some things with HTML, like adding embedded content. If you want more information on HTML, check out the [W3 Schools resources on HTML](https://www.w3schools.com/html/).

### Markdown

[Markdown](https://www.markdownguide.org/) is a plain-text markup language that makes it easy to format your text. Markdown converts what you write in words into HTML code that web browsers can read. Because it is so useful for writing, Markdown is an integral element to creating pages, projects, and posts on this site. This template has a guide on [Formatting Text with Markdown]({{ "/how-to/markdown/" | absolute_url }}), which you can check out later.

In the code, Markdown looks like this:

```
# title 
## subtitle
body text
```

This code will display on the website like this:

![Example title, subtitle, and body text in markdown ]({{ "/assets/images/example-markdown.jpg" | relative_url }})

### YAML

[YAML](https://yaml.org/) (YAML Ain't Markup Language) is an easy-to-read programming language that stores data on how your site should be built. For example, it can be used to set the titles, layouts, and permalinks of a page on your site, also known as variables. It is important to note that commands written in YAML are sensitive to line indentation. 

In code, YAML looks like this:

```yaml
# Site Settings
locale                   : "en-US"
title                    : "Critical Web Design Toolkit" 
name                     : "Digital Scholarship @ Bryn Mawr College" 
```
This is an excerpt of code from the yaml file called `_config.yml`. This file stores general information on the site as a whole:
- locale: set to "en-US" which means the site's language uses US English
- title: the title of the site
- name: name or organization, appears at bottom of the page

In the rest of this page, information stored in YAML such as "locale" and and "title" will be referred to as **variables**.

To learn more about YAML syntax, click [here](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started). 

## Using Markdown and YAML together 

You may use YAML, Markdown, and HTML together in your pages and projects. When YAML and markdown are used together, the YAML text or code is located at the top and called **front matter**. Front matter is always enclosed by triple-dashed lines like this `---`. To include any of the YAML variables on this page, all you need to do is copy and paste them into your front matter. 

### Editing the Homepage

Let's take a look at the template's default `index.md` file, which Jekyll uses to build the site's homepage. The front matter in that file looks like this:

```
---
layout: home
title: Critical Web Design Toolkit 
author_profile: false 

header:
    image: /assets/images/home.jpg  
    alt: "A large library with tall bookshelves and marble busts." 
    caption: "[Photo by Alex Block on Unsplash](https://unsplash.com/@alexblock)" 

sidebar:
    nav: "categories" 

include_categories:   
  - how-to # category
  - templates # category

classes: wide 
---
```

You can replace the text in this section with your own text, such as an introduction to your site. Here is what each new variable does:

**layout**:
- This sets the layout of the page. Since this is the homepage, layout is set to home. Other layouts are located in the `_layouts` file. 
    - It is not necessary to include a layout category, only our home page has a "layout" set

**author_profile**: 
- Setting this to true will display the site author information specified in _config.yml in this page's left sidebar

**header**: 
- Controls the large section of the page at the top
- As you can see, the category for "image" is indented. This tells the site to place the image *inside* the header
    - **image**: Putting the permalink path to an image here will add that image to this page's header
    - **alt**: short for alt text, used to describe an image
    - **caption**: provides an image caption which is good for citations. Here we included a link to the photographer

**sidebar**:
- creates the sidebar navigation. Does not need to be changed.

**include_categories**:
- divides the content on the page into categories 
- the bulleted items are the titles of the categories

**classes**:
- changes the formatting of the page. Shouldn't be changed.

In the home page or index.md file, the rest of the stuff after the enclosed front matter is the file's content or markdown section. The content looks like this:

```markdown
You can replace the text in this section with your own text such as an introduction to your site.

Below you will find instructions on how to install and configure your site as well as how to add and format your own content. 
You can safely delete them from your repository if you are done referencing them.
```

The text content in this section is written in Markdown (the text directly below the front matter that looks like plain, readable text), but you will notice that this section also contains some Liquid (in the curly brackets) and some HTML. This code adds some unique features to the homepage that Markdown itself cannot support. The Markdown text at the top of the section can be safely edited, but the Liquid and HTML code at the bottom should not be changed.


### Using YAML for other projects 

On other projects, there are several more variables that may be helpful to you that you can include in the front matter:

**permalink**:
- creates a path or link to the page
- each new page or project that you create in markdown *needs* a permalink
- to learn more, go to step 4, [Navigation]({{ "/how-to/navigation/" | absolute_url }}).

**teaser**: 
- the teaser makes an image appear on the front page display
- written as a permalink
- usually the same as a header image if you have one 

```
header:
    teaser: /assets/images/ocean-teaser-2.jpg 
```

It will appear on the home page like this:

![Example teaser image]({{ "/assets/images/example-teaser.jpg" | relative_url }})
    
**category**: 
- makes project to be visible on the home page using "spotlight"
- if you don't include category: "spotlight" your new page won't be visible on the homepage

```
category: "spotlight"
```

**toc:**
- stands for "table of contents"
- when set to true, automatically generates a table of contents on the side of a page
- **toc_label** is the title of the toc

```
toc: true;
toc_label: "On this page"
```

## Creating Your Own Pages and Projects

In your site repository, or location on GitHub, you will find two folders, one called `_pages` and one called `_projects`. By default, the files in `_pages` are what appear on the top navigation bar (`about.md` and `feedback.md`) of your site, while the files in `_projects` make up the instructional content that can be accessed from the home page. This may be a good model for structuring your site as well, but this is discussed more thoroughly in our [Navigation]({{ "/how-to/navigation/" | absolute_url }}) resource.

### Pages

We recommend the use of pages as a place to keep information that provides more general information about the whole website. Examples of pages that fit this description might be an About page or a Contact or Feedback page. Perhaps you want to include a page that lists all of the authors who contributed to the site. That, too, could be a good thing to include in `_pages`.

#### Editing Existing Pages and Creating Your Own

You may want to keep the existing `about.md` file and edit the YAML front matter and content section to be about your site instead. Feel free, also, to delete existing pages.

To create a new page, create a new Markdown (.md) file in the  `_pages` folder. In your new markdown file, you can copy and paste the front matter from the following example of an "Authors" page or from the code of the existing `about.md` page to get started. 

For example, to create a new page called "Authors," you would create a new markdown file called `authors.md` with the following front matter: 

```yaml
---
layout: single
permalink: /authors/ # should match the permalink in the navigation.yml file
title: Authors of this site #insert your preferred title here
header:
    image: /assets/images/default-1.jpg  # Putting the path to an image here will replace the header image.
    alt: "Describe your image here" # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image.
toc: true #creates a table of contents
toc_label: {{ page.title }} #label of toc is set to be the page's title
---
```

Keep in mind that the colors are only in the code to make it easier to read.

Then, once you have configured the YAML front matter to your liking, you can add text formatted with Markdown to the content section of the file.  

### Projects

Projects are a bit different. You can think of projects like individual blog posts or articles. This is where the main content and collected work that you want to organize and showcase lives on your site.

Looking at this site, our main content is a series of instructional written materials teaching you how to use this template, so all of these files were created in `_projects`. These can now be seen and accessed from the homepage in an organized way that you specify in the front matter of the `index.md` file, as discussed above.

#### Creating Your Own Projects

A good way to start making your own projects is to copy the code of the project template, '10_template.md'. 

First, though, you should create a file in the _projects section and name it with the following format: 00_filename.md, where you can replace 'filename' with whatever name you choose. 
- The two-digit number at the beginning of the filename will determine the order in which the "previous" and "next" buttons at the bottom of each project will navigate through the projects.

WE WILL WRITE MORE HERE
