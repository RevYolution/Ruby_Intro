## Layouts
- Allow for a template to wrap around the content of a page
- Create a directory `_layouts` where all of the templates will live
    ```Ruby
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
    ```Ruby
    ---
    layout: default
    title: Home
    ---
    <h1>{{ "Hello World!" | downcase }}</h1>
    ```
    Instead of having to have the whole HTML over several pages
- The `{{content}}` variable will render the content of the page that it is called on