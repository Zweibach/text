## basic terms

### downloader

#### GUG
Short for Gallery URL Generator. Takes a user input, such as `dog`, and turns it into a search query for a site such as safebooru like this: `https://safebooru.donmai.us/posts?page=1&tags=dog`. The resulting gallery URLs are then fed back into Hydrus and dealt with appropriately.

#### Preset
A term used for downloader settings found in a community managed downloader repository found here: [cuddle's repo](insert link here)
### downloader page

## settings

## dowloader types
URL, watcher, gallery, and simple downloaders are found under `download` in the pages drop-down menu in the menu bar or double-clicking the tab bar. Subscription is found under `network -> downloaders -> manage subscriptions` in the menu bar.

### url downloader
Easiest downloader to use. Give it one or more URLs and provided Hydrus recognises the URL Hydrus will download the content. Supports drag'n'dropping of tabs from browsers, bookmark entries, and some others. For copy-pasting there's the input box and if you have multiple URLs in your clipboard there's a notepad looking icon to the right of the input box.  
If you have direct links to files (URLs ending in things like .jpg, .png, .mp4) Hydrus can usually download them even without a parser.

### watcher
The downloader to use for downloading, for example, 4chan threads. Post a thread URL and let it run. All current images will be downloaded and the thread will be periodically checked for new images until the thread dies.

### gallery downloader
The go to downloader when you need to download a lot of something, such as all the art by an artist on some site. Requires a GUG for the site of interest.  
Select your gallery from the button under the input box (you can change the default for this in options) and then input the query the gallery is asking for in the input box. To the right of the input box there's a paste button for adding multiple queries, this will post each query as a separate download. Clicking the cog to the right of the paste button you can select some launch settings, including one that bundles all the separate queries into one download. This is recommended if you're doing a lot of small queries since Hydrus does not handle a lot of downloaders running at once well, or if you're doing queries where you expect a lot of overlap since it allows Hydrus to easily skip trying to redownload the same posts.  
Under the gallery button there's a setting for the number of files to check, running from 1 to unlimited.

### simple downloader
Useful if you're looking to do a one-off download from a page without having to actually write a full preset. Comes with some default formulae such as downloading all files linked in a page, all images linked in a page and some site specific formulae.

### subscription
Works a lot like the gallery downloader in that it needs a GUG and a query. The difference is in that subscriptions are intended to be periodic checks for new content of maybe a few hundred files per query.

sites

tags