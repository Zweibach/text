# Troubleshooting
**FIRST STEP: MAKE SURE YOU'RE ON THE LATEST VERSION OF HYDRUS**  
Depressingly often somebody comes and asks about issues that were solved and fixed already. Don't be that guy, update your Hydrus.

## Downloaders not grabbing content
**1. MAKE SURE YOU HAVE A PARSER FOR THE SITE**  
**2. MAKE SURE IT'S THE LATEST VERSION AVAILABLE**  
For Hydrus defaults you usually need to delete them and use the restore from defaults button. For ones taken from the presets repo check if there's a newer version there, delete what you have and import that. If not, well tough luck.

`Looks like HTML -- maybe the client needs to be taught how to parse this?`  
 - There's no parser for the content.
 
 `403`
  - Often happens with Cloudflare.

Flat out not downloading "random" posts.
 - If the site has posts hidden from normal users such as porn or paygated content you need to login via login script or by importing your cookies into Hydrus.

Using proxies.
 - Some sites base download limits on IP and not accounts even when logged in so if you are using the same VPN node as somebody else then there's a risk the limit has already been used or the node IP banned.