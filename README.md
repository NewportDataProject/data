---

---


# The Newport Data Project Data Repository
This is the location of our future repository for open datasets. The idea is to leverage the GitHub's support for [Jekyll](https://jekyllrb.com) to create an easy-to-use web interface for browsing and accessing the data. Beyond the technical aspects of creating the repository, we'll need to come through ways to handle data licensing.

## Why GitHub?

Importantly, _it's free_. We're resource-limited, so we take what we can get. But there are a lot of benefits (especially for a free package) that we should be able to take advantage of.

Git keeps a record of changes to files, which can [come in handy](https://blog.okfn.org/2016/11/29/git-for-data-analysis-why-version-control-is-essential-collaboration-public-trust/) for maintaining the integrity of a dataset and the analyses that use it. GitHub is designed for file sharing, so the workflow for uploading datasets is pretty natural for the tool. GitHub is also friendly to a [few types of data files](https://help.github.com/categories/working-with-non-code-files/) by providing some basic rendering to allow for easy preview in your browser, including mapping of geospatial data and a search function for tabular data files.

With GitHub pages there is a built-in user interface option (this page is running on it). With very limited effort we can have a clean, user-friendly front end for the data simply by adding markdown and html files.

## Technical Approach

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