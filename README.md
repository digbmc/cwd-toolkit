#The Critical Web Design Template

## Github, Jekyll and Visual Studio Code
Github is an online, cloud-based code hosting platform that helps to track and manage changes in Git repositories while enabling multiple people to work on a project at the same time. An essential part when it comes to using Github is having Git installed. Git is a version control system that help individuals to manage and keep track of their source code history.

Jekyll is a static site generator where it takes Markdown and HTML files and builds a static website based on the user’s preferred layouts. It has built-in support for Github for which it is a very useful tool when it comes to simplified site building.

Visual Studio Code is a code editing software which is used by individuals to edit the source code of a project or write new code using different programming languages such as HTML, CSS, JavaScript, etc. 

## Setting up Github
Follow the steps below to set up github and get started on your first project!

1. Sign up for a [Github account](https://github.com/join).

2. Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

3. To start a project, you have to create a new repository.
- Click on the “new repository” on the upper right-hand corner of Github. 
- Name your repository and check the box that states “initialize this repository with a README” .
- Click on “create repository”.

4. When you’re working on a project, it helps to have multiple versions of a repository at the same time. You need to create a branch to be able to edit the multiple versions at once. Everytime you create a new branch, it will be a copy of the main branch where you can make your new changes.
- To start a new branch, navigate to your new repository, click the dropdown that reads “branch: master”
- Type your desired branch name
- Click  “create branch.”

5. After making changes to a file in your branch, describe your changes by writing a commit message at the bottom of the page of that file which gives a short description of what changes have been made. The reason for having commit messages is to help other web developers understand how the project has progressed over time.

6. If you want the new changes you made in your branch to be merged with another branch, you have to open a pull request. A pull request is a notifying method to let the relevant parties involved in your project know about your request to merge your changes with another branch.
To open a pull request, go to the “pull request” tab and hit the button that says “new pull request.” 
After ensuring you like the changes you made in the new branch, click the “create pull request” button.
Title your pull request and briefly describe the changes. 
To finish, click “create pull request.”

7. In order to merge the branches, select the “merge pull request” button and click “confirm merge”.

**Forking a repository on GitHub**
If you want to directly edit the code in Github, you can fork our repository and start working from there. Forking a repository is basically making a copy of the original repository that you want to work with and this allows you to experiment with the code without affecting the original repository. To fork our repository, open our repository and click on the "fork" button towards the top right part of the screen.

**Cloning your repository and working locally**
You directly edit the code by forking a repository on Github but the drawback is that you have to wait a while before you get to see new changes that you made to your website. Hence, a good alternative to get rid of this issue is to clone the repository and work locally using a code editor like Visual Studio Code.

To clone our repository, follow the steps below:
1. Open [our repository](https://github.com/digbmc/ds-project) and click on the green "Code" button.
2. Copy the link that you see in the HTTPS tab.
3. Open git bash and type the following command and press enter.
```markdown
git clone ***paste the link that you copied in step 2 here***
```
4. See where in your computer the folder got cloned into and then open the folder of the cloned repository on Visual Studio Code and code locally. You can find more about this process in the section about "Using Visual Studio Code".

This [Github Documentation](https://docs.github.com/en/get-started) is a great resource to refer to if you want to learn more about Github.

## Working with Jekyll
Jekyll is a Ruby gem for which you need to install [Ruby](https://www.ruby-lang.org/en/downloads/) first.
After installing Ruby, open Ruby and run the command below to install Jekyll.

```markdown
 gem install jekyll bundler
```
 Jekyll has different themes that you may use to create your website. Our template is based on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme on Jekyll. 

[This documentation](https://jekyllrb.com/docs/) has more information about how Jekyll works.

## Using Visual Studio Code
If you decide to work locally, open the folder that you cloned from Github on Visual Studio Code and start coding. A major advantage for working locally is that you can preview the changes that you are making to your website almost instantly! 

**Pulling, pushing and commiting on Github through Visual Studio Code**
If you want to pull or push changes from another branch to yours, click the "Source Control" button on the left sidebar of Visual Studio Code. Then click on the three dotted lines on the top right of the panel that appears and you will see the pull and push options.

Before you can commit the changes you made, you have to "Stage" your changes. You can do that by clcking on the changes individually and click on the "+" button to stage the changes. After that, you can write a commit message in the box at the top of the panel and click commit.

To see how your website looks, click on "Terminal" at the menu bar and then select "New terminal". Make sure that you are in the folder where you are currently working on at the terminal. Then, type the following command in the terminal.
```markdown
bundle exec jekyll serve 
```
After running this command, find the line that has "Server address" and copy the link and paste it in your browser to view how your website looks like at that point of time.

## Minimal Mistakes and Reactor Room
Our template is based on a jekyll theme called [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/). This theme was built with the aim that individuals would use it for hosting their blog sites, personal sites, portfolio etc. The  programming languages that are used in this theme include HTML, SCSS, JavaScript and Ruby. 

Our Critical Webdesign Template is also inspired by [The Reactor Room](https://ds-pages.swarthmore.edu/reactor-room/). This website is a modified version of the Minimal Mistakes theme.


