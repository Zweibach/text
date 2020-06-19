# Tagless files and how to potentially solve it!

So you've installed Hydrus and imported your library of random images just to notice that none of them have any tags whatsoever. There are a number of ways to get tags without having to labour with tagging it all yourself. Though do keep in mind that these methods are limited to the type of content you have and its public availability. There's exceedingly little chance of your vacation images getting any tags from anywhere as an example.

This guide is not a replacement for the Hydrus [help documents](https://hydrusnetwork.github.io/hydrus/help/), it's just a guide for a prevalent and specific issue some people have. If you have any questions refer to the help documents.

## The Public Tag Repository
Or PTR to be short and sweet. It's a repository of filehash - tag relations. Adding it is as easy as click a button, see [help document page](https://hydrusnetwork.github.io/hydrus/help/access_keys.html). For further information see [this guide](https://github.com/Zweibach/text/blob/master/Hydrus/PTR.md). This method relies on another user having **that exact same file** and uploading tags for it to the PTR.  
If you're interested in using [QuickSync](https://cuddlebear92.github.io/Quicksync/) to get started it's best to do so before you import images as it overwrites the .db files.  
For downloading and syncing the "normal way" you can do that at any point, even after having imported hundreds of gigabytes of media. Update files are about 4GB to download but final database size is over 30GB and probably getting close to 40GB, processing takes a couple of days if your database files are on an SSD and quite a bit longer on HDD.

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
The recommended method for this is to use IQDB taggers from either [rachmadaniHaryono](https://github.com/rachmadaniHaryono/iqdb_tagger) or [nostrenz](https://github.com/nostrenz/hatate-iqdb-tagger). First one is a command line application while the latter has a graphical interface. Usage of both require you to be able to read their .README and google error messages.

There's a function found in `manage tags` for **a single file** that lets you lookup that image on IQDB. You can only do one image at a time and there's no automatation. Lookup scripts are also labeled as SEMI-LEGACY in Hydrus so don't expect much support on them.

## Using a neural network to tag
Precisely what it sounds like provided you know what it is. Deals primarily with anime and manga style art. Found [here](https://gitgud.io/koto/hydrus-dd/). Read the guide, follow it, google issues.