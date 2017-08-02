---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE5NiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.Z6qIXq477Nw1XC3kJz95HXHc0ON_F2POPPUaW4ZQC3o

title: >-
  Introduction to Jekyll
description: >-
  This lesson covers the basics of Jekyll and how to use it 
---
# What is Jekyll
Jekyll is a simple, static site generator. It uses a template directory which contains raw text files in various formats (either markdown or html), and runs it through  converters, and outputs a static website ready to be served.

Static site generators take source files, such as templates, style sheets, and blog posts and use them to generate websites. 

Although Jekyll is built to be blog-aware, it's important to point out that it's not blogging software in the traditional sense like Wordpress. It's simply a Ruby-based parsing engine that builds sites based on what you put into it. 

It is fast to load and gives you complete control over every aspect of your site.


# How it Works
Jekyll uses three main components to generate sites.
- **YAML** which stands for YAML Ain't Markup Language. This is used to store data, site variables, and what is known as _front matter_, which is information that tells Jekyll things like which layout to use for a post or page.
- **Liquid** is a Ruby-based templating language developed by Shopify. It's used to build templates that your pages are then constructed from. 
- **Markdown** is a text to HTML formatter that can be used to write content for individual posts or pages. You can also use HTML in Jekyll.


# Getting Started

### Installing Jekyll
- First you need to install the Jekyll gem from your terminal `gem install jekyll bundler`
- Now you can create a new Jekyll site by typing `jekyll new [sitename]` into your terminal. However, while this will create a site for you, it bundles all of the files and folders that you will need to access. Instead, we are going to use a boilerplate template I created: https://github.com/lexinamer/jekyllstarter

### Dissecting the Structure
![jekyll](https://s28.postimg.org/rj640x9v1/Screen_Shot_2016_12_14_at_11_50_30_AM.png)

- **_config.yml:** Jekyll uses a config.yml file for setting up configurations that will be used across your site. This can include things like the site name, collections, permalinks, and other things you will use globally across the site. 
- **_includes:** This folder is for partial views and small snippets that will go across your site. For example, header, footer, navigation, etc. 
- **_layouts:** This folder is for the main templates your content will be inserted into. You can have different layouts for different pages or page sections. For example, a portfolio layout for all portfolio pages, and default layout for main pages, etc. 
- **_posts:**  This folder contains your dynamic content/posts. the naming format is required to be `YEAR-MONTH-DATE-title.md`
- **css:** This is where your CSS will live. 
- **index.html:** This is your index or home page. 

### Running Jekyll
Just like with Sass, we have to process Jekyll to make it viewable on the web. Ultimately we will host this on Github using Github Pages, but for now we can run it locally on our machines.

Type `jekyll serve` into the terminal to make it run. You can then use a localhost in your browser to view your site. Note that this will also automatically compile your Sass for you so there is no need to Sass watch. 


### Other Tips
- The default layout takes content from your pages (index.html and menu.html) and inserts it into the ``{{content}}`` tag. The double squiggles are required and this is how you get the different template parts to your pages. 
- Include any scripts or fonts `<head>` tag inside the head section in the includes folder.
- Jekyll has some great documentation. Use it: http://jekyllrb.com/docs/home/
- Here is a helpful link on navigation: http://jekyll.tips/jekyll-casts/navigation/
- I would suggest using collections to organize all of your portfolio items instead of individual pages. This will make it easier to organize in the long run once you start adding more content. Here is a guide how to do it: http://newhaven.io/blog/creating-jekyll-portfolio-page/
- Be smart about your coding. Do you sketching first and **GET ORGANIZED** before you touch the code. 
- Feel free to add any additional folders on the root directory of your project. Such as images, js, etc. 
