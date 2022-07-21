---
title:  "2) Configuration"
category: "spotlight"
permalink: /how-to/configuration/
header:
    teaser: /assets/images/ocean-teaser-2.jpg 
    image:  # Putting the path to an image here will replace the header image.
    alt: "Dark ocean waves." # It is good practice to include an image desription as alt text.
    caption: "[Original Photo by Eric Han on Unsplash](https://unsplash.com/@madeyes)" # Put a caption for your image here. It will display in the bottom right corner of the image.
---

Now that you've forked the template repository and gotten set up in a code editing environment, it is time to configure your site's settings. This will be done by editing the code in your site's `_config.yml` file.

The `_config.yml`file is full of **comments** that help to tell you what each setting in the file does. The comments in this file begin with a pound/hash sign `#`, and they are sometimes used as headings to separate the code into sections or as notes next to items. Reading comments as you encounter them will ensure that you know what the code you are editing will change about your site.

## Locating _config.yml

To find the `_config.yml` file, scroll past the folders which appear at the top of the files. In a forked Github repository it should be the 8th file below the `assets` folder (Visual Studio Code may slightly rearrange the standalone files).

- To know you're in the right file, open it, and you should see the following:
![A message in the code that begins "Welcome to Jekyll! This config file is meant for settings that affect your entire site..."]({{ "/assets/images/configmessage.jpg" | relative_url }})

If the file you are in does not begin with this message, it is not the `_config.yml` file, and you should return to the main portion of the repository to locate it.

## Editing _config.yml

Before you begin adding other content and further customizing your site, you **must** change the following items in the `_config.yml` file so that your site will work as intended. When editing:
- Only change the text after `:` where you see the current information that appears on the template site.
- Write your information "in between quotation marks" as shown.
- Refer to the lefthand side of the code editor for **line numbers** (the # in parenthesis for each item below)

### Title (14)
![A red box surrounding Line 14 of code]({{ "/assets/images/configtitle.jpg" | relative_url }})

This is where you put your site title as you want it to appear in the browser tab and navigation bar. (Note that what appears in the browser tab can be different from the navigation bar. To do this, see "Masthead Title" later on this page.)

### Name, Description, URL (17-19)
![A red box surrounding Lines 17-19 of code]({{ "/assets/images/confignamedescurl.jpg" | relative_url }})

- **Name (17)**: Replace with your name, if you are the only contributer to your site, or your organization/class name if this site will host a group's collected work.
- **Description (18)**: Replace with a brief description of what your site is.
- **URL (19)**: Replace with the url of your site. This is based off of the github username with the forked repository and the repository name. By default, without changing the repository name, it should be https://githubUsername.github.io/ds-project. If you have changed your repository name, replace "ds-project" with the new name of your respository after the "/"

### Repository (21)
![A red box surrounding Line 21 of the code]({{ "/assets/images/configrepo.jpg" | relative_url }})

Replace with your repository name. Similar to the URL, the repository name here should match your forked repository and be based off the the github username with the forked repository. By default, without changing the repository name after forking, it should be githubUsername/ds-project. If you have changed your repository name, replace "ds-project" with the new name of your respository after the "/"

These are the only necessary changes to the `_config.yml` file.
The items below **can** be changed to update other parts of your site, but they do not have to be.

### Base URL (20)
The Base URL is the same as the repository name by default. If you want the baseurl to be something other than ds-project, you could change to something that reflects what your site is about instead. This process **requires** you to change your repository name in the `_config.yml` *and* officially on Github as well. This change will affect all portions of the site that use the repository name.

Here is the Github documentation for changing your repository name. Once you have done this, return to the `_config.yml` file and replace both the repository section and the Base URL section with your updated repository name. Make sure these match in all places.

### Locale (13)
Locale controls the language that the site displays in. It is set to English but can be changed if you would like to develop your site in a different language.

Search for the language you wish to develop your site in followed by the phrase "language code" in your preferred search engine, and replace the English code with the updated code for the language of your choice.

### Subtitle (16)
If you want to display a tagline on your site, add it here.

### Masthead Title (23)
If you want the title that displays in the top left of each page of your site to be different from the site's title, update this section with the preferred title for the page display.

### Search (56)
This theme comes with a built in website search function that you can enable by replacing "false" with "true" in this section.

The search function can be useful if your are compiling a lot of projects, but note that the formatting on the search window will likely be distorted.

Aside from these settings, you probably won't *need* to change much else in this file. You can read more about some of the other settings in the [Minimal Mistakes guide](https://mmistakes.github.io/minimal-mistakes/docs/configuration/), if you'd like, but it's not necessary.

Now we will discuss the next steps for setting up your site beyond the `_config.yml` file.

## Removing the Demo Site Content / Removing the content that comes with the template / Files you can safely delete after forking the repo

- All of the files in the `_projects` folder, including:
    - 01_installation.md
    - 02_configuration.md
    - ...
    - 10_template.md
- Any of the template's default images that you don't end up using
- README.md (or at least the content that is in it by default)

## Deploying the Site with GitHub Pages

Make sure that if you're working in a code editor like VS Code, that you push your changes to the main branch of your GitHub repository.

(Turn on GitHub Pages in repo settings?)

Preview your site
