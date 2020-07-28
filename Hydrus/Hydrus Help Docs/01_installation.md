[Back to table of contents](00_tableOfContents.md)
# Installing Hydrus

## Downloading
First step is to download Hydrus. Depending on the source this might double as installing it too.

[Official Github release](https://github.com/hydrusnetwork/hydrus/releases)  
Linux, MacOS, and Windows.  
If you're confident in installing dependencies you can also run from source.  
Only source guaranteed to be up to date, obviously.

[Chocolatey package](https://chocolatey.org/packages/hydrus-network)  
Windows.

[AUR package](https://aur.archlinux.org/packages/hydrus/)  
Linux.

[Docker hub](https://hub.docker.com/r/suika/hydrus)  
Docker.

## Installing
For at least a few of the above Hydrus will already be installed and ready to run. For the rest just follow normal procedure for installing software on your operating system of choice. The only thing to really keep in mind here is to put Hydrus on your fastest storage medium, preferably on an SSD.

If you're worried about space then you can use use the `migrate database` feature to put your media files on a slower drive with more space. The important part is that the database files (install folder/db, ends with .db) are on the quickest drive for best performance. Ignoring media files then a normal installation will after a while only require a couple of gigabytes of storage, maybe upwards of 4 GB if you have a really big library (millions of files with tags). Hydrus itself is a few hundred megabytes.  
If you're planning to run the Public Tag Repository (PTR) you will need about 40 GB.

## Updating
Hydrus does not have automatic updates. Release is usually once a week on Wednesdays. Just follow the steps you did for downloading and installing to update.

## Backups
To avoid loosing data, make sure to backup as often as possible or convenient. I do it at least once a week before updating Hydrus.  
Make sure Hydrus is turned off when launching external backup tools.

Hydrus has a built-in backup functionality. It is only available if you haven't used `migrate database` to split your storage. Even if you haven't using other backup solutions is still recommended.

Just copying and pasting the Hydrus folders. Not recommended.

[FreeFileSync](https://freefilesync.org/)  
Linux, MacOS, Windows.  
Recommended and used by dev and me. Somewhat basic but does the job well enough.

[Borg Backup](https://www.borgbackup.org/)  
FreeBSD, Linux, MacOS.  
More advanced and featurefull backup tool.

[Back to table of contents](00_tableOfContents.md)  
[Onwards to importing files](02_importAndExport.md)