# PTR for Dummies
or
## Myths and facts about the Public Tag Repository

### What is the PTR?  
Short for **P**ublic **T**ag **R**repository, a now community managed repository of tags. Locally it acts as a tag service, viewable under `services -> review services -> remote -> tag repositories -> public tag repository`. Here you can view its status, your account (default account when using Hydru's `help -> add the public tag repository` function is a public, shared, account. Currently only janitors and the administrator have personal accounts.), tag status, and how synced you are. Being behind on the sync by a certain amount makes you unable to push tags and petitions until you are caught up again. At the time of writing 39 million files have tags on it. The PTR only store the sha256 hash and tag mappings of a file, not the files themselves or any non-tag meta data. In other words: If you don't see it in the tag list it's not stored.

Everything in this document also applies to [self-hosted servers](https://hydrusnetwork.github.io/hydrus/help/server.html), except for tag guidelines.

### How does it work?
For something to end up on the PTR it has to be pushed there. Tags can either be entered into the tag service manually by the user through the manage tags window, or be routed there by a parser when downloading files. See [parsing tags](https://hydrusnetwork.github.io/hydrus/help/getting_started_downloading.html). Once tags have been entered into the PTR tag service they are pending until pushed. This is indicated by the `pending ()` that will appear between `database` and `network` in the menu bar. Here you can chose to either push your changes to the PTR or discard them.

- Adding tags pass automatically.
- Deleting (petitioning) tags requires janitor action.
- If a tag has been deleted from a file it will not be added again.
- Currently there is no way to re-add a deleted tag. If it's deleted it's gone.
- Adding and petitioning siblings and parents all require janitor action.

When making petitions it's important to remember that janitors are only human. We don't necessarily know everything about every niche. We don't necessarily have the files you're making changes for. Explain why you're making a petition. Try and keep the number of files managable. If a janitor at any point is unsure if the petition is correct they're liable to deny the entire petition rather than risk losing good tags. Some users have pushed changes regarding hundreds of tags over thousands of files at once, but due to disregarding PTR tagging praxis or being lazy with justification it's been denied wholesale.

`Q. Does this automagically tag my files?`  
`A. No. Until we get machine learning based auto-tagging nothing is truly automatic. All tags on the PTR were uploaded by another user, so if nobody uploaded tags associated with the hash of your file it won't have any tags in the PTR.`

`Q. How good is the PTR at tagging [insert file format or thing from site here]?`  
`A. That depends largely on if there's a scrapable database of tags for whatever you're asking about. Anything that comes from a booru or site that supports tags is fairly likely to have something on the PTR. Original content on some obscure chan-style imageboard is less so.`

### Janitors
Janitors are the people that review petitions. You can meet us at the community [Discord](https://discord.gg/3H8UTpb) to ask questions or see us bitch about some of the silly stuff boorus and users cause to end up in the PTR.

### Tag Guidelines

These are a mix of standard praxis used by various boorus and changes made by Hydrus Developer and PTR users, ratified by the janitors that actually have to manage all of this. The "full" document is viewable at [Cuddle's git repo](https://raw.githubusercontent.com/CuddleBear92/Hydrus-Presets-and-Scripts/master/tag%20guidelines). See Hydrus Developer's [thoughts on a public tagging schema](https://hydrusnetwork.github.io/hydrus/help/tagging_schema.html).

#### Siblings and parents
When making siblings, go for the closest less-bad tag. Example: `bad_tag` -> `bad tag`, rather than going for what the top level sibling might be. This creates less potential future work in case standards change and makes it so your request is less likely to be denied by a janitor not being entirely certain that what you're asking is right. Be careful about creating siblings for potentially ambiguous tags. Is `james bond` supposed to be `character:james bond` or is it `series:james bond`? This is a bit of a bad example due to having the case of the character always belonging to the series, so you can safely sibling it to `series:james bond`. But how about `wool`? Is it the material harvested from sheep, or is it the Malaysian artist that likes to draw Touhou? In doubtful cases it's better to leave it as is, petition the tag for deletion if it's incorrect and add the correct tag.

When making parents, make sure it's an always factually correct relationship. `character:james bond` always belongs to `series:james bond`. But `character:james bond` is not always `person:pierce brosnan`. Common examples of not-always true relationships: gender (genderbending), species (furrynisation/humanisation/anthromorphisism), hair colour, eye colour, and other mutable traits.

#### Namespaces
`creator:` Used for the creator of the tagged piece of media. Hydrus being primarily used for images it'll often be the artist that drew the image.  
`character:` Refers to characters. James Bond is a character.  
`person:` Refers to real persons. Pierce Brosnan is a person.  
`series:` Used for series. *James Bond* is a series tag and so is *GoldenEye*. Due to usage being different on some boorus chance is that you will also see things like Absolut Vodka it it.  
`photoset:` Used for photosets. Primarily seen for content from idols, cosplayers, and gravure idols.  
`studio:` Is used for the entity that facilitated the production of the file or what's in it. Eon Productions for the *James Bond* movies.  
`species:` Species of the depicted characters/people/animals. Somewhat controversial for being needlessly detailed, some janitors not liking the namespace at all. Primarily used for furry content.  
`medium:` Used for tags about the image and how it's made. Photography, water painting, napkin sketch as a few examples. White background, simple background, checkered background as a few others.  
`meta:` This namespace is used for information that isn't visible in the image itself or where you might need to go to the source. Some examples include: third-party edit, paid reward (patreon/enty/gumroad/fantia/fanbox), translated, commentary, and such.

Namespaces not listed above are not "supported" by the janitors and are liable to get siblinged out, removed, and/or mocked if judged being bad and annoying enough to justify the work. Recently `clothing:` was removed due to being disliked, no booru using it, and the person(s) pushing for it seeming to have disappeared, leaving a less-than-finished mess behind.