---
layout: single
permalink: /about/
title: About
header:
    image: /assets/images/home.jpg  # Putting the path to an image here will replace the header image.
    image_description: "Describe your image here" # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image.
toc: true
toc_label: {{ page.title }}
gallery:
  - url: /assets/images/home.jpg
    image_path: /assets/images/home.jpg
    alt: "placeholder image 1"
    title: "Image 1 title caption"
  - url: /assets/images/home.jpg
    image_path: /assets/images/home.jpg
    alt: "placeholder image 2"
    title: "Image 2 title caption"
  - url: /assets/images/home.jpg
    image_path: /assets/images/home.jpg
    alt: "placeholder image 3"
    title: "Image 3 title caption"
  - url: /assets/images/home.jpg
    image_path: /assets/images/home.jpg
    alt: "placeholder image 4"
    title: "Image 4 title caption"
---

This is an about page.

## Beverages
Coffee, tea, soda

## Foods
Fries, burgers, salads

### Sauces
Marinara, alfredo, homemade

### Condiments
Ranch, ketchup, 

## Animals
Giraffe, bear, cat

{% include gallery layout="half" caption="This is a sample gallery with **Markdown support**." %}