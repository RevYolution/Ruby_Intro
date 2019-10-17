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
