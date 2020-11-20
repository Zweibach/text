# Database migration
Read the official help doc [here](https://hydrusnetwork.github.io/hydrus/help/database_migration.html).

Databse migration is primarily used to put things that want fast drives (database and thumbnails) on fast drives and things that don't care (media files) in other places while all still being available to Hydrus.

The official help docs point out three components:
1. The installation
2. The database files
3. The media files

Thumbnails are part of #3 but can be assigned a separate location.

---

## Doing it
Easiest is if you do it before you actually start importing any images but doing it afterwards is no problem either.

### 1. The installation
You can put this pretty much wherever you want since it's only a few hundred megabytes at most. Only things to really keep in mind is that your user account has full right and read rights for the location. But if you have upwards of 50GB free (if you are using or intend to use the PTR) on an SSD then just install there.

If you want to move it after install it's pretty much as simple as copypasting it to the new location. If you used an installer you might need to rerun the installer and point to the new location to make sure all registries also point in the right direction but it's not actually important.

### 2. The database files
By default these are in the install directory which is why it's a good idea to install Hydrus on a fast drive with enough free space. The only real point I can see in putting databse files elsewhere is if you want to run "multiple" clients on a machine, more further down.

If you put the database files in a non-default location (that being ../Hydrus Network/db) you'll need a shortcut with a command line argument pointing to the directory the database files are in. I don't particularily recommend this so only do it if you actually have a clue what you're doing, see the official doc for further help and examples on this part.

### 3. The media files
Now these, these are the chunky ones especially if you have a lot of videos or the ridiculously oversized paywalled .pngs some artists provide.

The simple way is to turn off Hydrus, go to its install folder, down the db folder, find client_files and just moving it where you want it. When you start Hydrus again it'll warn you that it can't find the files and ask if you know where they are and point Hydrus towards the folder they are in now.  
The "proper" way is to open Hydrus, go to `database -> migrate database`, create a new location and crank its weight to 1 so the new location now says 100% files under "ideal usage". Hydrus will now move files over when running regular maintenance or you can click the `move files now` button to force it. You can have multiple locations with their own weights if you can't fit everything on a single drive or want to somewhat guard against drive failure (backups are the best protection!).

Do note that you have no control over what goes where, only how much.

### 3.5 The thumbnails
Ordinarily these are stored with the normal media files and if you change their location the thumbnails will come along. Unless you tell Hydrus to store them elsewhere.

Go to `databse -> migrate database` and look for "thumbnail location override" and just use the "set" button to, well, set it to a different location. Thumbnails are best put on a fast drive and don't use a lot of space. My 350k files use less than 4GB for example.

---

## Multiple clients
Using the function hinted at in #2 you can use a single install for multiple clients. Things are a lot easier when there's only one installation to keep up to date.

Some people use it for different types of content they don't want mixed.

**IMPORTANT:** Do not use the same location for the different clients' media since one client will look at files it's not supposed to have and throw it out making the other client(s) panic over missing files.