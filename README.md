# Ruby_Intro
Working on intro to Ruby

## Table of Contents
1. [Building a Site](/ruby_info/build.md)
1. [Liquid](/ruby_info/liquid.md)

## Building a site with Jekyll
- Jekyll is a static site generator
- Jekyll needs to build the site before it can be viewed
    `jekyll build`
- Jekyll can also build and reload with every change with
    `jekyll serve` which runs on `http://localhost:4000`

## Liquid
- Liquid is a templating language that has three parts
    - Objects
    - Tags
    - Filters

#### Objects
- Signify where to output content
- They are used with double curly braces
    `{{}}` for example `{{page.title}}` will output a variable with called `page.title` on the page

#### Tags
- Create logic and control flow for templating.
- They are used with curly brace and percentage sign
    `{%whateverLogicIsNeeded%}` 
- Example 
    ```ruby
    {% if page.show_sidebar %}
  <div class="sidebar">
    sidebar content
  </div>
    {% endif %}
    ```
    The above code will output the sidebar if `page.show_sidebar` evaluates to true
- [More on Tags](https://jekyllrb.com/docs/liquid/tags/)

#### Filters
- Change the output of a Liquid object
- They are contained within an output and are separated by a `|`
- Example `{{"hi" | capitalize }}` will output "Hi"
- [More on Filters](https://jekyllrb.com/docs/liquid/filters/)

## Font Matter
- YAML snippet that is set between two triple dash lines at the top of the page
    ```
    ---
    YAML snippet
    ---
    ```
- The `page` variable is where we can find the Font Matter variables
    ```ruby
    ---
    my_name: Jon
    ---
    {{page.my_name}}
    ```
    The above code would output "Jon" wherever `page.my_name`was found in the HTML doc

## Layouts
- Allow for a template to wrap around the content of a page
- Create a directory `_layouts` where all of the templates will live
    ```ruby
    <!doctype html>
    <html>
    <head>
        <meta charset="utf-8">
        <title>{{ page.title }}</title>
    </head>
    <body>
        {{ content }}
    </body>
    </html>
    ```
Above is an example of a default layout
- It allows for 
    ```ruby
    ---
    layout: default
    title: Home
    ---
    <h1>{{ "Hello World!" | downcase }}</h1>
    ```
    Instead of having to have the whole HTML over several pages
- The `{{content}}` variable will render the content of the page that it is called on