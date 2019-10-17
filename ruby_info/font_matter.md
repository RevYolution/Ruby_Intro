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
