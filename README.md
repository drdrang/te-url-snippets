These are the [TextExpander][2] snippets I use to capture the URLs of pages I'm browsing and, in some cases, transform them. They use either AppleScript directly or Python with the [appscript library][1] and work with both Safari and Google Chrome.

The multibrowser logic works this way:

1. If Safari is running, regardless of whether Chrome is running, get the URL from Safari.
2. If Chrome is running, and Safari isn't, get the URL from Chrome.


## furl ##

This is an AppleScript snippet that prints the URL of the frontmost tab of the frontmost browser window ("furl" = "front URL"). I use the abbreviation ";furl" to invoke it.

## 1url through 6url ##

These are AppleScript snippets that print the URL of the *n*th tab, counting from the left, of the frontmost browser window. I use the abbreviations ";1url" through ";6url" to invoke them.

## surl ##

This is an AppleScript snippet that prints the shortened URL of the frontmost tab of the frontmost browser window ("surl" = "shortened URL"). I use the abbreviation ";surl" to invoke it.

## 1surl through 6surl ##

These are AppleScript snippets that print the shortened URLs of the *n*th tab, counting from the left, of the frontmost browser window. I use the abbreviations ";1surl" through ";6surl" to invoke them.

## psurl ##






[1]: http://appscript.sourceforge.net/index.html
[2]: http://smilesoftware.com/TextExpander/
