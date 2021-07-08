# Tagless files and how to potentially solve it!

So you've installed Hydrus and imported your library of random images just to notice that none of them have any tags whatsoever. There are a number of ways to get tags without having to labour with tagging it all yourself. Though do keep in mind that these methods are limited to the type of content you have and its public availability. There's exceedingly little chance of your vacation images getting any tags from anywhere as an example.

This guide is not a replacement for the Hydrus [help documents](https://hydrusnetwork.github.io/hydrus/help/), it's just a guide for a prevalent and specific issue some people have. If you have any questions refer to the help documents.

If you're in this position even after using Hydrus to download the files there's a few reasons why:
1. You're a dumfuck who didn't read the docs. See here: [parsing tags](https://hydrusnetwork.github.io/hydrus/help/getting_started_downloading.html#parsing_tags).
2. You did read the docs but forgot to set tag parsing to default on for new pages/downloaders/whatever. Go to `network -> downloaders -> manage default tag import options` and do that.
3. Tag parsing for that site is temporarily broken due to recent site changes or something. Wait for a Hydrus update (usually every Wendsday) and hope it gets fixed, or see if there's a new version on the Github/Discord server.

When you've solved the problem all you need to do is select the files, righ-click and copy all known URLs and paste them into an URL downloader page. Don't forget to enable the correct settings in `tag import settings` of that page.

## The Public Tag Repository
Or PTR to be short and sweet. It's a repository of filehash - tag relations. Adding it is as easy as click a button, see [help document page](https://hydrusnetwork.github.io/hydrus/help/access_keys.html). For further information see [this guide](https://github.com/Zweibach/text/blob/master/Hydrus/PTR.md). This method relies on another user having **that exact same file** and uploading tags for it to the PTR. The reason for this is that Hydrus uses hashes to identify files, see [what is a hash?](https://hydrusnetwork.github.io/hydrus/help/faq.html#hashes) in the official help docs.  
If you're interested in using [QuickSync](https://koto.reisen/quicksync/) to get started it's best to do so before you import images as it overwrites the .db files.  
For downloading and syncing the "normal way" you can do that at any point, even after having imported hundreds of gigabytes of media. Update files are about 4GB to download but final database size is about 50-60GB, processing takes a couple of days if your database files are on an SSD and quite a bit longer on HDD.

Refer to the article on [database migration](https://hydrusnetwork.github.io/hydrus/help/database_migration.html) if your SSD isn't big enough to fit your database files *and* your media.

## Tagging files on import
This option hinges on you not having deleted your files after importing them into Hydrus. If you did then that's on you, hopefully you have a method of recovering from it.

When you were importing your files into Hydrus you probably used the `file -> import files` option and if you did you probably saw the two buttons labeled `import now` and `add tags before importing >>`.  
It's the second one you want. There's options for conserving file names as tags (useful if the filename contains useful information or if you just want it preserved), folders as tags, using regular expressions, or importing tags from a .txt file. The last one requires the textfile to have the same name as the file that should receive the tags and be in the same directory. Preserving this information can be useful if you wish to, for example, export an image from Hydrus with its old filename.

## Using file hash to search sites that support hash searches
This works best for anime and manga style images. It hinges primarily on there being a site with the file and you not having saved samples (booru images usually have `sample` in its filename and Pixiv has `_master1200` as examples) or downsampled images from Discord or imgur or other similar sites and services.

For how to do it there's a guide here: [How to fetch tags in bulk with md5 hash](https://github.com/CuddleBear92/Hydrus-Presets-and-Scripts/wiki/2.-How-to-fetch-tags-in-bulk-with-md5-hash).

## Using IQDB and Saucenao
Deals primarily with anime and manga.  
The recommended method for this is to use IQDB taggers from either [rachmadaniHaryono](https://github.com/rachmadaniHaryono/iqdb_tagger) or [nostrenz](https://github.com/nostrenz/hatate-iqdb-tagger), or the SauceNao tagger from [GoAwayNow](https://github.com/GoAwayNow/HydrausNao). Rachmadani's and GoAway's are command line applications/scripts and requires you to have Python while nostrenz's has a graphical interface and does not require Python. Usage of either require you to be able to read their README and google error messages.

There's a function found in `manage tags` for **a single file** that lets you lookup that image on IQDB. You can only do one image at a time and there's no automatation. Lookup scripts are also labeled as SEMI-LEGACY in Hydrus so don't expect much support on them.

## Using a neural network to tag
Precisely what it sounds like provided you know what it is. Deals primarily with anime and manga style art. Found [here](https://gitgud.io/koto/hydrus-dd/). Read the guide, follow it, google issues.