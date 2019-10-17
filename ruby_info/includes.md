## Includes
- The `include` tag allows the addition of content in the `_includes` folder
- These are useful for having a place for code that is repeated over the site in several places
- Navigation is a good use tool for the `includes` tag

```Ruby
<nav>
  <a href="/">Home</a>
  <a href="/about.html">About</a>
</nav>
```
The above code can be held in `_includes/navigation.html`
```Ruby
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>{{ page.title }}</title>
  </head>
  <body>
    {% include navigation.html %}
    {{ content }}
  </body>
</html>
```
When put in a `_layout/default.html` like above the navigation will be rendered where the `{% includes navigation.html %}` is present

#### Useful variables
- Jekyll can utilize the `page.url` variable to highlight the current page with the following logic
```Ruby
<nav>
  <a href="/" {% if page.url == "/" %}style="color: red;"{% endif %}>
    Home
  </a>
  <a href="/about.html" {% if page.url == "/about.html" %}style="color: red;"{% endif %}>
    About
  </a>
</nav>
``` 
Within the code above the `{% if page.url == "whateverpage" %}` will check the url. If it is equal to what is in the quotes it will change the color of the link to red. 