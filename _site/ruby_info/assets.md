## Implementing CSS, JS and Images within a project
- Like most projects CSS, JS and Images are held within an assets folder
- [Sass](https://sass-lang.com/) is baked into Jekyll
- Sass is a great way to structure CSS rules that are complied for us

#### Setup for Styling 
- Within the css folder in the assets folder have a `styles.scss` document
- Start with the code below
    ```Ruby
    ---
    ---

    @import "main";
    ```
- The empty front matter signifies to Jekyll that it needs to process a file
- `@import "main";` tells Scss to find a file named `main.scss` in a directory called `_scss`

