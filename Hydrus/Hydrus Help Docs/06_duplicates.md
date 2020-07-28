[Back to table of contents](00_tableOfContents.md)
# Duplicates
Hydrus has a system for detecting and managing duplicates. Currently the detection system only works for static images but you can manually tell Hydrus to queue up files as potential duplicates to then make a decision on them.

The dupe page is found under `new page -> special -> duplicates processing`.

Manually marking as potential duplicates are done by marking multiple files and right-clicking them then navigating `manage -> file relationships -> set relationships -> set all possible pair combinations as 'potential' duplicates for the duplicate filter.`

## Preparation
Unless you have manually set potential duplicates you have to head to the tab labeled as `preparation`. By clicking the cog icon you get a menu where you can reset potential duplicates and set Hydrus to automatically do dupe searches when system is idle.

Search distance is how similar images need to be to be flagged as duplicates. The `Exact duplicate` setting already catches a lot, such a differences in facial expressions, semen/no semen variants, censoring/no censoring, colour/greyscale, and other small variants. Colour, file size, and aspect ratio doesn't matter to being found as duplicates but will affect weight (weights are found and edited under `file -> options -> duplicates`) when running the dupe filter.

Click the `Play` looking button to start the search and then head on over to the next tab when it's done.

## Filtering
Go to the `filtering` tab to get started doing filtering. Check the `edit default duplicate metadata merge options` to know what Hydrus will do when you pick any of the filter options. Do note that filter decisions aren't final until you exit the filter and press `commit` when asked about your decisions. If you think you've done wrong you can step back by pressing the arrows or just press `forget` to discard all decisions.

Keybinds/shortcuts can be found under `file -> shortcuts -> media viewer - duplicate filter` or by hovering the decision buttons in the dupe filter.


[Back to table of contents](00_tableOfContents.md)  
[Onwards to API](07_api.md)