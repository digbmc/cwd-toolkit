---
layout: single
# code: This is where you paste your embed code if you want it to get displayed at the bottom of the page.
title:  "This is a post with embedded content"
date:   2022-07-05 10:00:00 -0400
category: "How-To"
header:
    teaser: /assets/images/default-4.jpg
    # image: /assets/images/home.jpg  # Putting the path to an image here will replace the header image.
    image_description: "Describe your image here" # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image.
# map: This is where you put the embed code of the Google Map.
---

Embedding refers to the integration of links, images, videos, gifs and other content into social media posts or other web media. For example, you are visiting a site such as Khan Academy and you see a youtube video there. The youtube video that you see on the website is an embedded content. 

To embed any type of content, you would need an embed code first. An embed code is a block of HTML that is placed in another page and renders a visual element — a video, social media post, form, or page — from another website or source.
<a href="https://blog.hubspot.com/marketing/embed-social-media-posts-guide" style="color: purple; text-decoration: underline;">You can follow this detailed guide to get the embed code for any type of content.</a>

## Steps to embed content:
1. To embed any type of content, change the first line of the markdown file where you want to embed your content to layout: single. This will apply the single.html layout on your respective markdown file.

2. After getting the embed code, paste it beside code: **paste the embed code here** in the second line of the markdown file. If you don't see any "code:" in the first few lines of the file, you can type it yourself and paste the embed code beside it as shown previously.

3. To format the embedded content, you can change the height and width in the embed code itself that you put at the top of the markdown file according to your preferred dimensions. You have to put specific values for the height and width such as 500; percentages are not accepted.

4. Save the changes and view the content that you just embedded. As an example, you can see an embedded video of how to draw cats below.
>  <iframe width="800" height="450" src="https://www.youtube.com/embed/Y-ObdZ6fw60" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Other things that you can embed:
<hr>

* If you want to embed a Google Map as shown at the bottom of the page, follow step 2 but put the embed code of the Google Map beside map: **paste the embed code here** at the top of the markdown file or you could just follow the first bullet point stated in the next section if you want the map to be in a specific position in the website.
> <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d24440.49827767732!2d-75.3074176!3d40.0293888!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sus!4v1657129930385!5m2!1sen!2sus" width="550" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
* If you want to make a timeline for your project(s), you can follow this <a href="https://timeline.knightlab.com/" style="color: purple; text-decoration: underline ;">guide</a> to create a timeline. You will also find the embed code of your timeline in this guide which you can use to embed the timeline on the website.

## Other things that you can do to or with your embedded content:

* If you want to change the position of your embedded content, one easy way of doing it could be by just pasting the embed code in your desired place in the markdown file if you don't want it to be at the bottom of the page. This applies to any type of embedded content.
* If you want to apply some other layout to your page but if the layout doesn't have the coding that allows you to embed content, you can just add the code shown below at any part of the file based on where you want the embedded content to show up. 
> <img src="/assets/images/embedded-responsive.png" alt="This is how the embed code should look like more or less." style="height: 73px; width: 100%;"/>


<br/>
