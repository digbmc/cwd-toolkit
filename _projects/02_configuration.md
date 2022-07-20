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

The `_config.yml`file is full of **comments** that help to tell you what each setting in the file does. The comments in this file begin with a pound/hash sign `#`, and they are sometimes used as headings to separate the code into sections or as notes next to items.

## Locating _config.yml

## Editing _config.yml
Values that you MUST change:
- title
- name
- description
- url (format: https://githubUsername.github.io/repoName)
- repository (format: githubUsername/repoName)
Values that you can change:
- baseurl (if you want the baseurl to be something other than ds-project, you could change to something that reflects what your site is about; remember: no spaces; IMPORTANT NOTE: baseurl MUST match the repository name, so you must also change the repo name, both on GitHub and in the _config.yml file, to match your new baseurl)
- locale (changes site language; will also change the language the site's built-in features like the "next" and "previous" buttons)
- subtitle (if you want to add a site tagline)
- masthead title (if you want the title that displays in the top left of each page of your site to be different from the site's title)
- search (you can change the value of search (line 56 of `_config.yml`) to true or false to enable or disable a search bar on you site)

Aside from these settings, you probably won't *need* to change much else in this file. You can read more about some of the other settings in the [Minimal Mistakes guide](https://mmistakes.github.io/minimal-mistakes/docs/configuration/), if you'd like, but it's not necessary.

## Removing the Demo Site Content / Removing the content that comes with the template / Files you can safely delete after forking the repo

- All of the files in the `_projects` folder, including:
    - 01_installation.md
    - 02_configuration.md
    - ...
    - 10_template.md
- Any of the template's default images that you don't end up using
- README.md (or at least the content that is in it by default)

