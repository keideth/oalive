# FREELINKING PREPOPULATE README.md

## CONTENTS OF THIS FILE

TBA

## INTRODUCTION

Freelinking Prepopulate provides freelinking plugins that leverage the
Prepopulate module to link to Drupal form pages that are partially
preloaded.

The following items will be inherited from the the parent node and
used to prepopulate the new node:

* Title
* Book outline (requires the **Book** module to be enabled).
* Taxonomy term  (requires the **Taxonomy** module to be enabled).
* OG context  (requires the **OG** module to be enabled).

**Note:** *Taxonomy term* does not work and is disabled. *OG context* is not yet tested.

For example, the following freelink: `[[Does not exist]]`,  produces:

    <a class="freelink freelink-createnode notfound freelink-internal" title="node/add/article" href="/node/add/article?edit%5Btitle%5D=Does%20not%20exist&parent=836">Does not exist</a>

Here, the `parent=836` identifies the book the new node shall be part of.


## REQUIREMENTS

Requires [Prepopulate][1].


## RECOMMENDED MODULES

* [Markdown filter][1]:<br>
  When this module is enabled, display of the project's `README.md` will be
  rendered with markdown when you visit `/admin/help/freelinking_prepopulate`.


## CREATENODE

The create node module links to a node/add page. It is used primarily
as a failover for the Nodetitle plugin.  When this module is enabled,
the failure option "Add a link to create content" is added to the
pull down menu.

In that case, the *Identifier* is treated as a title, and used to
preload the node/add form's title field. 

With advanced configuration, it can also preload the currently viewed
book parent, or organic group. These advanced fields only work when
viewing text on a particular node page.

### FREELINKING PREPOPULATE UTILITIES

The Freelinking Prepopulate Utilities
(`freelinking_prepopulate.utilities.inc`) are intended to help with
the centralized definition of form fields that may be of interest for
Prepopulate-based plugins, and automating the process of extracting
information for such fields.


## MAINTAINERS

* [grayside](https://www.drupal.org/u/grayside)
* [juampy](https://www.drupal.org/u/juampy)
* [gisle](https://www.drupal.org/u/gisle)


[1]: https://www.drupal.org/project/prepopulate
[2]: https://www.drupal.org/project/markdown
