---
title:  "Site Navigation"
category: "spotlight"
permalink: /how-to/navigation/
---

Your site has two main navigation bars: the masthead navigation at the top of each page and the sidebar navigation on the left side of most pages. The contents of both of these navigation bars are determined by the navigation.yml file in the site's _data directory. Let's look at each type of nav bar separately.

## Masthead Navigation

The items in the masthead navigation are determined by the 'main' section of the navigation.yml file. The default 'main' section looks like this:
```yaml
# main links
main:
  - title: "Home"
    url: /
  - title: "About"
    url: /about/
  - title: "Feedback"
    url: /feedback/
```
Each item in the section is indented and begins with a hyphen and a space, and each item has two attributes: title and url. The title attribute determines the text that will be displayed for that item in the nav bar, while the url should be the permalink of the page you want that item to link to. The order of the items in this list determines their order in in the rendered navigation bar.

If you're not sure what items should go in this navigation section, it's a good idea to add the links to each of your site's pages (not your projects). The files for your pages should be located in the site's _pages directory with the exception of the index.md file, which acts as your site's homepage.

Feel free to add new items or delete existing ones from the navigation.yml file's 'main' section, but try not to add too many items to the masthead navigation, as it may break the masthead's formatting. If you have a lot of pages or projects that you would like to include in a navigation bar, consider using the sidebar navigation instead.

## Sidebar Navigation

By default, your site's homepage and each project page includes a sidebar navigation menu. If you would like to add a sidebar nav to a page in your _pages directory, add these lines to the YAML front matter of that page's file:
```yaml
sidebar:
     nav: "categories"
```
On the other hand, if you would would like to remove the sidebar nav from a page that has one by default, add this line to the front matter of that page's file:
```yaml
sidebar: false
```
By default, the items in the sidebar navigation are determined by the 'categories' section of the navigation.yml file, which looks like this:
```yaml
# sidebar links
categories:
  - title: "Getting Started"
    children:
      - title: "Installation"
        url: /how-to/installation/
      - title: "Configuration"
        url: /how-to/configuration/
  - title: "How-To"
    children:
      - title: "Formatting Text with Markdown"
        url: /how-to/markdown/
      - title: "Images"
        url: /how-to/images/
      - title: "Embedded Content"
        url: /how-to/embedded-content/
      - title: "Bibliography"
        url: /how-to/bibliography/
  - title: "Templates"
    children:
      - title: Project Template
        url: /templates/project/
```
Each item in the 'categories' section (each one indented and beginning with a hyphen and a space) represents a subsection with a title attribute, which displays as a section header in the sidebar nav, and a set of 'children.' Each child of each section is further indented and also begins with a hyphen and a space. Then, similar to the items in the masthead navigation, each child has its own title, which renders as the link's visible text, and url, which should match the linked page's permalink.

To customize the sidebar to suit your needs, edit the 'categories' section of the navigation.yml file, maintaining the proper syntax and structure, as shown above.

It is also possible to [create custom sidebars for individual pages](), in case you wanted a different sidebar nav to display on different pages. However, we recommend that you stick with just the one for the sake of consistency and accessibility, since navigation that is inconsistent across the pages on a site can frustrate or impede users.

You can also take a look at the Minimal Mistakes documentation on navigation:
- [Minimal Mistakes Navigation](https://mmistakes.github.io/minimal-mistakes/docs/navigation/)
- [Minimal Mistakes Custom Sidebar Navigation Menu](https://mmistakes.github.io/minimal-mistakes/docs/layouts/#custom-sidebar-navigation-menu)
- [Minimal Mistakes Sidebar Navigation List Example](https://mmistakes.github.io/minimal-mistakes/layout-sidebar-nav-list/)