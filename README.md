# Timeselector - DokuWiki-Helper-Plugin-Version

Providing the functionality of [Zhao Xiaodong's timeselector jQuery plugin](https://github.com/nicolaszhao/timeselector) for DokuWiki

  * *Original version: https://github.com/nicolaszhao/timeselector*
  * *This version: https://github.com/hh-lohmann/timeselector/tree/dokuwiki-helper-plugin*


## UNDER CONSTRUCTION - TO DO:

### *creating helper.php*


### *creating plugin.info.txt*


### *usage advice here*

  - ... from other plugins
  - ... from within HTML parts in wikitext (if allowed in the wiki)



### *test under DokuWiki release Binky*


### *test under DokuWiki release Ponder Stibbons*


### *publish http://dokuwiki.org/plugin:timeselect*


## CONSTRUCTION NOTES - DONE:

### *reducing stuff*

#### *deleting /demo*

#### *deleting /libs*

#### *deleting /src/.jshintrc*

#### *deleting /test*

#### *deleting CONTRIBUTING.md*

#### *deleting .jshintrc*

#### *deleting Gruntfile.js*

#### *deleting package.json*

#### *timeselector.jquery.json*

### *applying DokuWiki plugin file structure, preserving nicolaszhao's original file structure*

**We want to fit DokuWiki's plugin file structure, but we want also to keep nicolaszhao's original file structure for timeselect (e.g. for future updates)**

#### *script.js*

[DokuWiki wants](https://www.dokuwiki.org/devel:plugin_file_structure#javascript) a script.js, thankfully sporting [a special include mechanism](https://www.dokuwiki.org/devel:javascript#include_syntax)

#### *style.css*

[DokuWiki wants](https://www.dokuwiki.org/devel:plugin_file_structure#css_styles) a style.css, thankfully CSS allows for an ```@import``` of CSS files in CSS files

