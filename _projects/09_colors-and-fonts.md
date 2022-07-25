---
layout: single
title:  "Colors and Fonts"
category: ["how-to"]
permalink: /how-to/colors-and-fonts/

header:
    teaser: /assets/images/header-5.jpg
    overlay_image: /assets/images/header-5.jpg  # Putting the path to an image here will replace the header image.
    image_description: "Bundle of yellow roses." # It is good practice to include an image desription as alt text.
    caption: "[Photo by Annie Spratt on Unsplash](https://unsplash.com/@anniespratt)" # Put a caption for your image here. It will display in the bottom right corner of the image.
    show_overlay_excerpt: false

sidebar:
    nav: "categories"

toc: true;
toc_label: "On this page"

---

You can change the look of your site using options called "skins," and you can also edit colors and fonts in the site's `.scss` files. Don't worry, you don't have to comb through all of the site's `.scss` files to do this. Making changes in a couple files will apply settings across your whole site.

## Skins

You can easily change the site's whole color scheme by changing the skin in the `_config.yml` file. The template comes with a few pre-made skins that are available for your use, including the default skin, which is called "academic." The skin options are listed in `_config.yml` under "Theme Settings."
```yaml
# Theme Settings
remote_theme: "mmistakes/minimal-mistakes@4.24.0"
skin    : "academic" # Minimal Mistakes: "default", "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"; CWDT: "academic"
```
You can also make your own skin or edit an existing one, if you would like. The code for skins is located in the _sass folder. 

```
.
├── _sass
    └── minimal-mistakes
        └── skins
```

You can either edit the code for the skin you would like to edit directly in that skin's file, or you can create a new skin file, copy the code of one of the existing skins into your new file, and make edits there. The new skin file should be named according to the following format: `_name.scss`, where 'name' can be a word of your choice. To use your new theme, put its name in quotes after "skin:" in `_config.yml`.

## Changing Colors

Most of the code in this template uses hex values, series of six letters and numbers, to denote colors. VS Code has built in color pickers, but if you are not using VS Code, you can access an [online hex color picker](https://htmlcolorcodes.com/color-picker/). 

Skins set the default the color scheme across your whole site. The code in each skin file will look something like this:

```
/* Colors */
$background-color: #eae0d4 !default; // light brown
$text-color: #000000 !default; // black
$muted-text-color: #555761 !default; // gray-blue
```

To edit the colors in a skin, change the hex values, or numbers and letters that come after each hashtag. Code editors like VS Code make this easy to do with a graphic interface for picking colors, but you can also copy hex values from online color pickers.

You can also edit colors on specific elements using HTML and CSS, effectively overriding the skin's defaults. To find out more about this, check out the [W3 Schools HTML Tutorial](https://www.w3schools.com/html/) and [CSS Tutorial](https://www.w3schools.com/css/default.asp). 

## Changing Fonts

Unlike colors, fonts are not a part of skins. To change the fonts, access the `_variables.scss` file in `_sass/minimal-mistakes`. 

```
.
├── _sass
    └── minimal-mistakes
        └── _variables.scss
```

The variable that changes fonts is called `font-family`. To change the fonts across the whole site, you can change the values for the typeface variables in the `_variables.scss` file. You can edit the fonts listed in the `$serif`, `$sans-serif`, and `$monospace` variables.
```
/* system typefaces */
$serif: Georgia, Times, serif !default;
$sans-serif: -apple-system, BlinkMacSystemFont, "Roboto", "Segoe UI",
  "Helvetica Neue", "Lucida Grande", Arial, sans-serif !default;
$monospace: Monaco, Consolas, "Lucida Console", monospace !default;
```
Then, specify which sections of text use serif, sans-serif, and monospace fonts by editing the following variables.
```
$global-font-family: $sans-serif !default; // for main content text
$header-font-family: $serif !default; // for headers
$caption-font-family: $serif !default; // for image captions, etc.
```
