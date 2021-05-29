# Downloader troubleshooting step-by-step
Or
### People keep doing dumb stuff that's easily overlooked all the time (me included) so here's a checklist

1. Make sure you're logged in and that the site works.
2. Check that you actually have a working parser.
3. Update your Hydrus.
4. Delete the old parser and import/restore it.
5. Repeat all steps as necessary.

###### The URL is dumb! :chadYes:

### 1. Make sure you're logged in.
Most reliable is to just go to the site, login there, and then use the Hydrus Companion to send the cookies to Hydrus. Some sites have login scripts available in Hydrus, either by default or as a downloader import. Delete old cookies before you do this. Also go to the site either way to check that it works.

### 2. Check that you actually have a working parser.
The Cuddlebear downloaders repository. If it doesn't exist or is outdated either fix it yourself or pray somebody else cares enough to waste their time on your problem.

### 3. Update your Hydrus.
Just update your damn Hydrus.

### 4. Delete the old parser and import/restore it.
Go into the gallery url generators, url classes, and parser management panels (found in `network > downloader components`), select anything related to the troublesome site and delete them. Then either use the add defaults button to add them back in, or re-import the downloader objects.

### 5. Repeat all steps as necessary.
Yes, really.