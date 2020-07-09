# Tags and ratings
[Back to table of contents](00_tableOfContents.md)

The primary tools used for finding things in your library. They come in a few different flavours. 

**System predicates are system assigned tags.** Things like filesize, pixelcount, aspect ration, filetype, has audio, has duration/no duration, URL, and some statistics or dupe system related ones. Just to name a few. Give them a look and read them properly, they can be quite powerful for searching.

**Assigned tags.** Tags that are assigned by a user to a file. Stuff like who made it, what it depicts, and whatever else you can think of that is useful for finding the image again.

**Ratings.** Things like scoring 1 to 5 or like/dislike as examples. You can use them for quite a lot of things. I have a rating I use for whether a comic strip is tagged well enough to be easily found or not.

## Tags
To manage tags you either press F3 (the default manage tags shortcut), or right-click a file and navigate `manage -> tags`. This launches the `manage tags` window and the entry field should be focused. If not it's the empty box below the button that says "remove all/selected tags". Writing here will run a search for tags in your database and display the results below. It lets you auto-complete, can be navigated with your arrow keys and you can select multiple tags at once by holding in either shift or control and clicking the tags you want. Pressing enter will add the highlighted tag(s) to the list of tags above which is the tags on the file(s). Press "Apply" to apply the tags or "Cancel" to cancel and discard all changes.

Beneath the `manage tags` title bar there's one to several tabs. Default is one named `my tags`. These are known as tag services and you always have one local (local meaning it only exists in that client) and can freely create more. Like with ratings further down you navigate `services -> manage services` in the menu bar and add a local tag service.  
Tag services are useful if you want to segregate certain types of tags or other organisational purposes. I for example have a service I parse downloaded tags into and one exclusively for tags I add manually.

If you're downloading from a booru you're likely to see things like `creator:`, `character:`, and `series:`. These are called namespaces, useful for disambiguation, grouping, and searching.

### Siblings
Also known as *alias* on some boorus. Maybe you're downloading from multiple boorus and they each have tags that mean the same thing, but are written differently. Maybe one writes it as `thighhighs` while another does `thigh-highs`. With siblings you can tell Hydrus that `thigh-highs -> thighhighs`, allowing you to find both tags when searching for either.

### Parents
Also known as *implication* on some boorus. An always correct tag relationship can be made to have one be the parent of the other. Very common example on the Public Tag Repository is characters and series. `character:ash ketchum` is always from `series:pokémon` so can be given the relation `character:ash ketchum -> series:pokémon`. This way `series:pokémon` will always be added to files with the `character:ash ketchum` tag.

## Ratings
To use this feature you must create a rating service. Navigate to `services -> manage services` in the menu bar then add a rating service of your choice. There's currently two to pick from. Numerical rating, going from 0 to some undefined high value. And like/dislike rating, which has three values: Positive, negative, unrated. With the `system:rating` predicate you can use ratings in searches, so if you want to see `blonde hair` images you've liked or given `x` numbers of stars to, you can.

[Back to table of contents](00_tableOfContents.md)  
[Onwards to searching and sorting](05_searchingAndSorting.md)