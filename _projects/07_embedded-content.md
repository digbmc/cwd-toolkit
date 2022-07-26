---
title:  "Embedded Content"
category: "how-to"
permalink: /how-to/embedded-content/

header:
    teaser: /assets/images/embedded-header.jpg
    image: /assets/images/embedded-header.jpg  # Putting the path to an image here will replace the header image.
    alt: "Paintings in a gallery" # It is good practice to include an image desription as alt text.
    caption: "[Original Photo by Zalfa Imani on Unsplash](https://unsplash.com/@zalfaimani)" # Put a caption for your image here. It will display in the bottom right corner of the image. # Put a caption for your image here. It will display in the bottom right corner of the image.

embed-code: # This is where you paste your embed code.
---

Embedding refers to the integration of links, images, videos, gifs and other content into social media posts or other web media. For example, you are visiting a site such as Khan Academy and you see a youtube video there. The youtube video that you see on the website is an embedded content. 

## Embed Code
To embed any type of content, you would need an embed code first. An embed code is a block of HTML that is placed in another page and renders a visual element — a video, social media post, form, or page — from another website or source.
<a href="https://blog.hubspot.com/marketing/embed-social-media-posts-guide" style="color: peach; text-decoration: underline;">You can follow this detailed guide to get the embed code for most of the types of content.</a>

## Steps to embed content
1. The first thing you should do is decide the position where you want to embed the content in the markdown file.
2. Paste the embed code that you obtained in the position that you decided on the markdown file.
3. To format the embedded content, you can change the height and width in the embed code itself according to your preferred dimensions. You have to put specific values for the height and width such as 500; percentages are not accepted.
4. Save the changes and view the content that you just embedded. As an example, you can see an embedded video of how to draw cats below.
 <iframe width="800" height="450" src="https://www.youtube.com/embed/Y-ObdZ6fw60" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
 
**Formatting wide content**
To add content that you want to fill the entire page width, we recommend that you set the page layout to "wide" and remove both the sidebar and Table of Contents to ensure that your embedded content will fit the screen as desired (these are the settings for the second example project including the ArcGIS Storymaps about National Parks).

### Other contents that you can embed
* If you want to make a timeline for your project(s), you can follow this <a href="https://timeline.knightlab.com/" style="color: peach; text-decoration: underline ;">guide</a> to create a timeline. You will also find the embed code of your timeline in this same guide which you can use to embed the timeline on your website.
* If you want to embed a Google Map as shown below, follow step 2 from "Steps to Embed Content". 
 <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d24440.49827767732!2d-75.3074176!3d40.0293888!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sus!4v1657129930385!5m2!1sen!2sus" width="740" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

## Using Liquid syntax for embedded content
If you want to embed different contents at a specfic position in multiple pages on your website, you can use liquid for making the process easier. Liquid is a templating language Jekyll uses to process pages on your site. With Liquid you can output and modify variables, have logic statements inside your pages and loop over content. This is to give an overview of what Liquid does but you don't have to know about Liquid to be able to use this template!

1. Go to the layout file that the pages where you want to embed different contents are using and insert this code snippet either above or below the content section based on your preference. If you find this code snippet present in the layout already then you don't have to do anything and can skip to the next steps. However, this would mean that all of your embedded contents would show up at the bottom of each page so if you want to change this position then place the code snippet in your desired position.

```markdown
{% raw %}
 {% if page.embed-code %} <div class="embed-responsive"> 
          {{page.embed-code}}
        </div> {% endif %}
{% endraw %}
```
2. You can then come back to each of those markdown files and paste the embed code of those different contents as instructed in the next step.
3. Paste the embed code beside embed-code: **paste the embed code here** at the top of the markdown file. If you don't see any "embed-code:" in the first few lines of the file, you can type it yourself and paste the embed code beside it as shown previously. 
