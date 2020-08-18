# Downloading
One of the primary features of Hydrus is its ability to download from a wide range of sites. This page covers terms, types, and basic guiding.  
Quick basic guide for which you want to use:
 - Chan threads: Watcher
 - Everything with specific tag(s): Gallery downloader
 - Singular posts or pages: URL downloader
 - One-off from some site not otherwise supported: Probably the simple downloader
 - Periodic checking and downloading of tag(s): Subscriptions

## Basic terms

### Downloader
The component Hydrus needs to interact with a site and understand what it receives from a site. Consists of a few different parts, described below.

#### GUG
Short for Gallery URL Generator. Takes a user input, such as `dog`, and turns it into a search query for a site such as Safebooru like this: `https://safebooru.donmai.us/posts?page=1&tags=dog`. The resulting gallery URLs are then fed back into Hydrus and dealt with appropriately.

#### URL classes
> The fundamental connective tissue of the downloader system is the 'URL Class'. This object identifies and normalises URLs and links them to other components. Whenever the client handles a URL, it tries to match it to a URL Class to figure out what to do.

Without an URL class Hydrus has no idea what to do with any URLs sent its way. URL classes are linked to parsers, this is usually done automatically but you can also do it manually in case you want to swap out a parser for one with a different functionality.

#### Parsers
The component that figures out what is what in a page. Extracts image URL, tags, source URL, time stamps, and whatever else useful information a site might provide.

#### Login script
Many sites hides things from users that are not logged in. A login script will allow Hydrus to act as if it is logged into a site with the credentials you provide it. Especially useful for blacklisting or avoid automatic blacklists, access to increased rates if you have some form of premium account, or other features limited to logged in and/or paying users. Do mind rate limits though since Hydrus is not responsible for your account potentially getting banned due to misuse.

#### HTTP header
HTTP headers pass additional information with requests. Examples include browser agent, cookies, origin, and so on.

#### Session cookies
Cookies, plain and simple if you've ever used a browser. It's what tells the site that you are logged in. By importing them to Hydrus you can bypass the need for a login script which is useful since some sites are tricky to get a login script to work, but trivial to import the cookies into Hydrus.

#### Bandwidth rules
Rules for downloading. There's global, downloader page, subscription, and site specific rules that you can set as desired. You can set data cap and number of requests over a specified period. Such as 10GB per day, 100 requests per hour, 5 requests per second as an example.  
You can also throttle download speed by setting the period to data per second.

#### Preset
A term used for downloader settings found in a community managed downloader repository found here: [cuddle's repo](https://github.com/CuddleBear92/Hydrus-Presets-and-Scripts). Commonly includes everything that's needed to download from a site using Hydrus' downloader pages. Sometimes also called *all in one*.

### downloader page
A downloader page is simply one of the listed below downloaders open in a tab.

### Gallery/file log
In any downloader page or subscription query there's a button that looks like three columns of thin lines. Hovering over it should show the text `open detailed gallery log--right-click for quick actions, if applicable`.

## Settings
Editing default file import options: `file -> options -> importing`  
Editing default tag import options: `network -> downloaders -> manage default tag import options`  
Editing default downloader options: `file -> options -> downloading`

### File import options
Regards to known URLs and hashes and what to do when ecountering one. Minimum and maximum filesize and resolution, what to do with files and such.

### Tag import options
Default parsed tags service, known URLs and hashes and what to do when encountering one. Default tag blacklist and whitelist. Can be set per parser.

### Downloader options
Icons used, default GUG, how often to run subscriptions and watchers by default, default search limit, etc.

# **Downloader types**
URL, watcher, gallery, and simple downloaders are found under `download` in the pages drop-down menu in the menu bar or double-clicking the tab bar. Subscription is found under `network -> downloaders -> manage subscriptions` in the menu bar.

### URL downloader
Easiest downloader to use. Give it one or more URLs and provided Hydrus recognises the URL Hydrus will download the content. Supports drag-and-dropping of tabs from browsers, bookmark entries, and some others. For copy-pasting there's the input box and if you have multiple URLs in your clipboard there's a notepad looking icon to the right of the input box.  
If you have direct links to files (URLs ending in things like .jpg, .png, .mp4) Hydrus can usually download them even without a parser.

### watcher
The downloader to use for downloading, for example, 4chan threads. Post a thread URL and let it run. All current images will be downloaded and the thread will be periodically checked for new images until the thread dies.

### gallery downloader
The go to downloader when you need to download a lot of something, such as all the art by an artist on some site or all images with a specific tag. Requires a GUG for the site of interest.  
Select your gallery from the button under the input box (you can change the default for this in options) and then input the query the gallery is asking for in the input box. To the right of the input box there's a paste button for adding multiple queries, this will post each query as a separate download. Clicking the cog to the right of the paste button you can select some launch settings, including one that bundles all the separate queries into one download. This is recommended if you're doing a lot of small queries since Hydrus does not handle a lot of downloaders running at once well, or if you're doing queries where you expect a lot of overlap since it allows Hydrus to easily skip trying to redownload the same posts.  
Under the gallery button there's a setting for the number of files to check, running from 1 to unlimited.

### simple downloader
Useful if you're looking to do a one-off download from a page without having to actually write a full preset. Comes with some default formulae such as downloading all files linked in a page, all images linked in a page and some site specific formulae.

### subscription
Works a lot like the gallery downloader in that it needs a GUG and a query. The difference is in that subscriptions are intended to be periodic checks for new content of maybe a few hundred files per query. Do mind that subscriptions are not intended to function as a gallery downloader so if you want everything from a query it's recommended to first run a gallery download of it and then add it as a subscription.

sites

tags