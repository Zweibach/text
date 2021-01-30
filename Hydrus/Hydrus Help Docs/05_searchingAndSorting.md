[Back to table of contents](00_tableOfContents.md)
# Searching and sorting
The primary purpose of tags is to be able to find what you've tagged again. For this we have the search feature of Hydrus.

## Searching
Just open a search/files page and start typing away in the search field which should be focused when you first open the page.

Hydrus will treat a space the same way as an underscore when searching so the query `hydrus network` will find files tagged with `hydrus network` and `hydrus_network`.

Tags will be searchable by all its siblings. If there's a sibling for `large` -> `huge` then the query `large` will find files tagged with either and so will a search for `huge`. This goes for the whole sibling chain, no matter how deep or a tag's position in it.

### System predicates
Tags are intended to tell you about content in the file while system predicates on the other hand deals with the files themselves for the most part: How big a file is, resolution, number of pixels, sound or no sound, number of tags assigned to the file, time imported, and quite a few other things. System predicates are the things prefixed with `system:` in the window that appear when you click in the search box.

### OR searching
Hydrus supports OR searching, aka searching for two or more tags and presenting all files that have at least one of the tags. For example the query `red eyes` OR `green eyes` will present you with files that are tagged with red eyes or green eyes or both.

The simple version is to write a query, hold shift and double-clicking the tag you want to press enter for selected tag(s). This will add them to a string of OR queries at the top of the tag search list. You can keep adding tags to the string. Just run the string as a query by double-clicking it or marking+enter key it.

There's a more advanced OR search function available by pressing the OR button. Previous knowledge of operators expected and required.

## Sorting
At the top-left of most pages there's a `sort by: ` dropdown menu. Most of the options are self-explanatory and those that aren't you can just test them out. They do nothing except change in what order Hydrus presents files to you.

Default sort order and more `sort by: namespace` are found in `file -> options -> sort/collect`.

## Collecting
Collection is found under the `sort by: ` dropdown and uses namespaces listed in the `sort by: namespace` sort options. The new namespaces will only be available in new pages.

[Back to table of contents](00_tableOfContents.md)  
[Onwards to duplicates](06_duplicates.md)