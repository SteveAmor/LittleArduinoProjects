# The Catalog

This is a simple Javascript catalog for building the
[LittleArduinoProjects GitHub Pages site](https://leap.tardate.com).

It is a simple bootstrap/datatables page with the main entry point in [index.html](../index.html).
Catalog data is loaded from [catalog.json](./catalog.json), which is consolidated from `.catalog_metadata` I've added to each project.

The [make.py](./make.py) utility script is used to maintain the catalog:

```
$ catalog/make.py rebuild  # regenerates catalog from the README.md
$ catalog/make.py generate  # builds the catalog from catalog metadata
```


## Atom Feed

The [make.py](./make.py) script also generates the [atom.xml](./atom.xml) feed file.
This is a best-effort conversion to an atom feed. Currently includes all projects in the feed.

* [feed validator](http://www.feedvalidator.org/check.cgi?url=https%3A%2F%2Fleap.tardate.com%2Fcatalog%2Fatom.xml)
* [published feed location](https://leap.tardate.com/catalog/atom.xml)


## Hosting

I'm using [Netlify](https://www.netlify.com/) to run the catalog site directly from the GitHub repository.

Note: I previously used GitHub Pages, but switched to NEtlify as that allows me to use free SSL certificates from [LetsEncrypt](https://letsencrypt.org/).


## Credits and References
* [Netlify](https://www.netlify.com/)
* [LetsEncrypt](https://letsencrypt.org/)
* [GitHub Pages](https://pages.github.com/)
* [bootstrap](http://getbootstrap.com)
* [datatables](http://datatables.net/)
* [..as mentioned on my blog](https://blog.tardate.com/2016/06/littlearduinoprojects-now-with-fancy.html)
