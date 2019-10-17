## Data Files
- Jekyll allows for loading data from several different files as long as they are contained in a `_data` folder
    - [YAML](https://yaml.org/)
    - JSON
    - CSV
- Having files separate from the source code can allow for easier maintenance of a site. 

#### Using YAML
- It is possible to use YAML as an array of navigation items as shown below
```Ruby
- name: Home
  link: /
- name: About
  link: /about.html
```
- Jekyll uses the above by accessing `site.data.whateverfile`
- This use allows to iterate over the data instead of having to dirty the HTML with more links that are so similar
- To change the HTML add the required material to the `.yml` data file