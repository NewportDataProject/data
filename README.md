---

---
# THE PORTAL HAS MOVED!
## For datasets, please check out [github.com/newportdataportal](https://github.com/newportdataportal).
This repository will stick around in case the ideas or code could be useful for any projects, but it should be considered inactive.

# The Newport Data Project Data Repository
This is the location of our future repository for open datasets. The idea is to leverage the GitHub's support for [Jekyll](https://jekyllrb.com) to create an easy-to-use web interface for browsing and accessing the data. Beyond the technical aspects of creating the repository, we'll need to come through ways to handle data licensing.

## Adding data to the repository
The repository uses jekyll [collections](http://jekyllrb.com/docs/collections/) as the framework.  To add a dataset:  
1. Fork the repository.
2. Create a new folder in the `_datasets` directory, named after the dataset.
2. Create an 'index.md' in the new folder, filling in the yaml frontmatter:  

```
---  
layout: dataset  
title: YOUR_TITLE  
description: YOUR_USEFUL_DESCRIPTION  
---  
```  
3. Put your datafiles in the folder.
3. Submit a pull request.

## Approach

#### Build the data repository inside the website file structure

We want to take full advantage of Jekyll for the front end, so we need to make sure the back end is compatible with Jekyll's [file structure](http://jekyllrb.com/docs/structure/).  
* Use jekyll [collections](http://jekyllrb.com/docs/collections/)

#### Use templates to build the navigation interface

Jekyll supports [templates](http://jekyllrb.com/docs/templates/) to present content in a standard format, and includes logic that we can use to traverse the file structure. Combined with JavaScript like [this](https://www.w3schools.com/howto/howto_js_filter_table.asp), we should be able to build a relatively useful interface.

#### Upload workflow

To start, the clone/pull-request method can work for uploading datasets, but we can look at ways of using APIs to streamline uploads.

#### Programmatically generate pages for datasets

Since Jekyll can take care of the formatting and navigation logic for us, it should be fairly straightforward to write offline scripts that can generate `index.md` files based on the dataset's metadata. We should also be able to embed GitHub renderings of certain types of data files directly on the page.

#### Download workflow

Not every user will want to download the entire repository, so we need to provide a reasonable way to access a particular dataset. It will probably end up using links to raw github files.
