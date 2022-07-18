---
layout: single
title:  "Customizing skins"
category: ["how-to"]
permalink: /how-to/custom-skins/

header:
    teaser: /assets/images/default-4.jpg
    overlay_image: /assets/images/default-4.jpg  # Putting the path to an image here will replace the header image.
    image_description: "" # It is good practice to include an image desription as alt text.
    caption: # Put a caption for your image here. It will display in the bottom right corner of the image.

sidebar:
    nav: "categories"

toc: true;
toc_label: "On this page"

---

Customizing the website's overall appearance, also known as its "skin," is made simple using CSS. In the code for this project, you will find the skins located in the _sass folder. 

```
.
├── _sass
    └── minimal-mistakes
        └── skins
```

For example, the skin that this current site is using is called "academic." 

Changing the current skin to default versions already built in from Minimal Mistakes is simple. All you need to do is go to the `_config.yml` file and change the `minimal_mistakes_skin` to the title of the one you want. 

```yaml
# Theme Settings

theme                  : "minimal-mistakes-jekyll"
minimal_mistakes_skin    : "academic-blue" # "default", "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"
```
There are a handful of options available, including our default skin for this site is called "academic." In order to customize the colors, create a new file in the skins folder and copy and paste the code from the "academic" skin. 

## Colors

Our code uses hex values, a series of six letters and numbers, to denote colors. To be directed to a color picker for hex values, click [here](https://htmlcolorcodes.com/color-picker/). 

To further edit the skins' colors, you can edit directly in the skin scss files. 

The code will look something like this:

```
/* Colors */
$background-color: #eae0d4 !default; // light brown
$text-color: #000000 !default; // black
$muted-text-color: #555761 !default; // gray-blue
```

To edit the colors, change the hex values, or numbers and letters that come after each hashtag. For reference, the hex value for black is #00000 and white is #fff, and other colors are combinations in between. 


## Fonts

To change the fonts, access the _variables.scss file located in the vendor folder. 

```
.
├── _sass
    └── minimal-mistakes
        └── vendor
        └── _variables.scss
```

The variable that changes fonts is called `font-family`. There is generally a font-family code element for each element of the site that includes text listed in their respective scss folder. However, a simple way to change the fonts for the whole site are in the variables file:

```
$global-font-family: $serif !default; // for large chunks of text
$header-font-family: $serif !default; // for headers
$caption-font-family: $serif !default; // for image captions, etc.
```
