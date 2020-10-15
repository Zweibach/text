# Pixiv

## Not getting R-18 content
If you are encountering the issue that you can't download any R18 art from Pixiv even though you are logged in with the login script in Hydrus, the following is likely the case:

The Pixiv login in Hydrus is currently broken and does not work. It is flat out removed on new installs. Due to technical limitations it will still falsely report that you are logged in after a login attempt, even though you are in fact not.

This can not be fixed at the moment since the Hydrus login system is missing certain abilities it would require to deal with the reCAPTCHA v3 Pixiv is using.

For now, please disable the login in Hydrus and delete all the existing cookies for Pixiv. Then, copy the login cookies into Hydrus manually or – recommended – via [Hydrus Companion](https://gitgud.io/prkc/hydrus-companion).

If you decide to use Hydrus Companion, you can also set it up to send the cookies to Hydrus automatically in certain intervals, removing the need to keep doing it manually. The interval should be set short enough so the Pixiv login cookies won't expire before it is sent again (it currently seems to last 30 days, so setting something like 7 days in Hydrus Companion should put you on the safe side).

## 403/Cloudflare error in downloaders
Pixiv recently did *something* causing Hydrus and other scraping utilities to hit Cloudflare if logged in, presumably as an anti-bot measure. See [this](https://github.com/Nandaka/PixivUtil2/issues/814#issuecomment-708224059) PixivUtil2 issue for more info. Current workaround is to just change your Pixiv password. Remember to delete cookies in Hydrus before reimporting them to be safe.