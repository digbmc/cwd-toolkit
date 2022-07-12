---
layout: home
title: Site Title
author_profile: false # Setting this to true will display the site author information specified in _config.yml in this page's sidebar.

header:
    image: /assets/images/home.jpg  # Putting the path to an image here will replace the header image.
    image_description: "Describe your image here" # It is good practice to include an image desription as alt text.
    caption: "[Photo by Alex Block on Unsplash](https://unsplash.com/@alexblock)" #Add a visible caption to your image or give credit to the photographer or source.

sidebar:
    nav: "categories"

include_categories:   
  - how-to
  - templates

entries_layout: grid # Choose how to display posts. Options: grid, list.

classes: wide # Setting the class as wide will extend the page's content into the right margin.
---

You can replace the text in this section with your own text such as an introduction to your site.

In each of the posts below you will find instructions on how to add certain features. All of these posts have the "How-To" category. You can safely delete them from your repository if you are done referencing them. 

You will notice each post has its own teaser image. You can specify what that image is in the YAML front matter (the code at the top of the file between the two sets of `---`) on each post. If a post is made with no teaser image specified in its YAML front matter, then your site will display a default teaser image, which you can set easily. Just delete the 'teaser.jpg' file in the /assets/images folder and replace it with the file of an image of your choice. Make sure you rename your new image file 'teaser.jpg'.

<div class="spotlight"> 
{% assign spotlight_projects = site.projects | where: 'category', 'spotlight' %}
{% include spotlight projects = spotlight_projects %}
</div>

{% for c in page.include_categories %}
<div id="{{ c }}" class="pane">
<h3>{{ site.data.content.display_categories[c] }}</h3>
{% assign category_projects = site.projects | where: 'category', c  %}
{% include collection_row projects = category_projects %} 
</div>
{% endfor %}