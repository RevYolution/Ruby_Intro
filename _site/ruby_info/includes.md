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