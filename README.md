# Term Search

This module uses Backdrop's core search to index taxonomy terms. The default
behavior will index taxonomy terms from all vocabularies with any fields
rendered on the main display, however this behavior can be customized in various
ways.

## Features

Administrators can choose which vocabularies get indexed for search.
Adds a 'Search Index' display mode option for vocabularies so searchable fields
can be customized. Administrators should make sure the display mode is enabled
in the vocabulary's 'Manage Display' tab, and select which fields should be
indexed.

Provides hooks to add custom text to the search index or search results for each
term.

## Requirements

Must have the core Search, Field and Taxonomy modules enabled.

## Installation

Install this module using the official Backdrop CMS instructions at
<https://backdropcms.org/guide/modules>.

## Configuration

Navigate to the `admin/config/search/settings` page,
and check the 'Term Search' box under Active Search Modules.
After saving, you can also choose which vocabularies
are indexed for search in the "Indexed Vocabularies" fieldset.

(optional) You can run cron manually to begin indexing terms, or wait for it to
happen over time.

(optional) Visit the manage display page for a taxonomy, and set which fields s
hould display on a search result.

The module also allows other modules to interact with the indexing and searching
process, by invoking either `hook_term_update_index()` or
`hook_term_search_result()`.

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for complete text.

## Current Maintainers

[Herb v/d Dool](https://github.com/herbdool/)

This module is currently seeking co-maintainers.

## Credits

Ported to Backdrop by [Herb v/d Dool](https://github.com/herbdool/)

Drupal maintainers are: [scotthorn](https://www.drupal.org/u/scotthorn).
