---
layout: single
title:  "All About Images"
category: ["how-to"]
permalink: /how-to/images/

header:
    teaser: /assets/images/default-1.jpg
    overlay_image: /assets/images/default-1.jpg  # Putting the path to an image here will replace the header image.
    image_description: "Describe your image here" # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image.

toc: true
toc_label: "On this page"

gallery:
  - url: /assets/images/default-1.jpg
    image_path: /assets/images/default-1.jpg
    alt: "placeholder image 1"
    title: "Image 1 title caption"
  - url: /assets/images/default-2.jpg
    image_path: /assets/images/default-2.jpg
    alt: "placeholder image 2"
    title: "Image 2 title caption"
  - url: /assets/images/default-3.jpg
    image_path: /assets/images/default-3.jpg
    alt: "placeholder image 3"
    title: "Image 3 title caption"
  - url: /assets/images/default-4.jpg
    image_path: /assets/images/default-4.jpg
    alt: "placeholder image 4"
    title: "Image 4 title caption"
---
<!-- command + ?/ to create an HTML comment -->
<!-- (This is a post with a gallery, and we can write about how to add a gallery to any post or page here.) -->
<!-- 
```markdown

```
 -->
=======

Want to learn more about putting in images into your website? You've come to the right place. 

## The Basics

### Adding images

<<<<<<< HEAD
At this point, you might have added a post or two, and want to start adding some of your own images—exciting! The most basic way to include image is by using plain old YAML markdown. 

At this point, you might have added a post or two, and want to start adding some of your own images—exciting! The most basic way to include an image is by using plain old YAML markdown. 

1. Upload the image into the images folder, located in assets
2. Link the uploaded image in your code

In the code, it looks like this:


<!-- the tick marks represent example code-->

```markdown
> ![image description](/assets/images/default-1.jpg))
```

Here is the outcome:

![test image](/assets/images/default-1.jpg)

The text in the brackets [] is called **alt text**, or an image description, which is written in the code but not visible on the site. It is important to *always* include alt text because it not only clarifies your code, but it also visibilizes the text to screen readers, making the image more accesible.

### Imbedding images from online sources

Let's say you would like to include an image from the web, such as in a library database or digital gallery. All you need to do is put the link to the image into the markdown code for images. The image will appear in the place where you place your line of code. 

Let's say you would like to include an image from the web, such as in a library database or digital gallery. All you need to do is put the link to the image into the markdown code for images. The image will appear in the location where you place your line of code. 

In the code, it looks like this:

```html
> ![Cat on shoe shine stand](https://tile.loc.gov/storage-services/service/pnp/ppmsca/75100/75128v.jpg))
> <figcaption> Cat on shoe shine stand taken by Angelo Rizzuto in 1960. Anthony Angel Collection (Library of Congress). </figcaption>
```
Here is the outcome:

![Cat on shoe shine stand](https://tile.loc.gov/storage-services/service/pnp/ppmsca/75100/75128v.jpg)
<figcaption> Cat on shoe shine stand taken by Angelo Rizzuto in 1960. Anthony Angel Collection (Library of Congress). </figcaption>


Here, I've linked a photo from the Library of Congress to the page. As long as it is still visible on the linked website, it will be visible on yours. 

To learn more about Markdown syntax click [here](https://www.markdownguide.org/basic-syntax/) 

### Adding captions 

In order to add captions to your post, you can use an HTML command in Minimal Mistakes called <code>figcaption</code>. All you need to do is enclose your text in the following HTML syntax and place it beneath the image in your Markdown code, as seen above. 

```html
<figcaption> Your Caption Here. </figcaption>
```

## Image Galleries

One of the most basic ways of displaying multiple images is through a **gallery**. Galleries are grids of images which can be modified and tailored however you want. To put in a gallery, you can use a type of code syntax called **Liquid**. Liquid is a templating language used in Jekyll that communicates with HTML code and your YAML front matter to call the gallery and make it appear. Its syntax is characterized by curly brackets: {}. 

For example, if I want to input an image gallery below, I would use the following liquid code: 

<!-- I'm using the "raw" command so that the computer prints the code instead of reading it literally -->
{%raw%} 
```
{% include gallery caption="Here I've changed the caption." %}
```
{%endraw%}

The result looks like this: 

{% include gallery caption="This is a sample gallery with **Markdown support**." %}

By changing the layout to "half," we get a two-column gallery: 

{% include gallery layout="half" caption="Here I've changed the caption." %}

In the code, it looks like this: 

{%raw%}
```
{% include gallery layout="half" caption="Here I've changed the caption." %}
```
{%endraw%}

For galleries, you can update the gallery **caption** by using the command <code> caption="text" </code> and including it in the liquid code. To change the captions of each individual image, you need to input each caption in the YAML front matter under <code>title</code>, which will be visible if you click on the image. 

For individual image captions, the front matter looks like this:

```yaml
gallery:

    - url: /assets/images/default-1.jpg
    image_path: /assets/images/default-1.jpg
    alt: "placeholder image 1"
    title: "Image 1 title caption"

    - url: /assets/images/default-2.jpg
    image_path: /assets/images/default-2.jpg
    alt: "placeholder image 2"
    title: "Image 2 title caption"

    - url: /assets/images/default-3.jpg
    image_path: /assets/images/default-3.jpg
    alt: "placeholder image 3"
    title: "Image 3 title caption"

    - url: /assets/images/default-4.jpg
    image_path: /assets/images/default-4.jpg
    alt: "placeholder image 4"
    title: "Image 4 title caption"

```

However, the front matter will not create a gallery on its own, and you must **call** your gallery by using the Liquid syntax from before. Where you place the Liquid is where the gallery appears.

To learn more about creating galleries in Minimal Mistakes, click [here](https://mmistakes.github.io/minimal-mistakes/post%20formats/post-gallery/)

### What does layout do?

Adding the layout feature / code changes how many columns are displayed in the gallery. In order to change the three column default, I wrote <code>layout="half"</code> which specifies that I want two columns side by side instead of three columns.  

Excluding the layout command from the liquid code would revert to the three-column gallery default. 

## Going Further

### Resources

- To learn more about Liquid syntax, click [here](https://cloudcannon.com/community/learn/jekyll-tutorial/introduction-to-liquid/#:~:text=What%20is%20Liquid%3F,can%20just%20start%20using%20it.)

- To learn more about creating galleries in Minimal Mistakes, click [here](https://mmistakes.github.io/minimal-mistakes/post%20formats/post-gallery/)

- To learn more about embedding images, click [here](https://medium.com/markdown-monster-blog/getting-images-into-markdown-documents-and-weblog-posts-with-markdown-monster-9ec6f353d8ec
)

- To learn more about image captioning and embedded content with Minimal Mistakes, click [here](https://mmistakes.github.io/minimal-mistakes/docs/helpers/)

