These are the [TextExpander][2] snippets I use to capture the URLs of pages I'm browsing and, in some cases, transform them. They use either AppleScript directly or Python with the [appscript library][1] and work with both Safari and Google Chrome.

The multibrowser logic works this way:

1. If Safari is running, regardless of whether Chrome is running, get the URL from Safari.
2. If Chrome is running, and Safari isn't, get the URL from Chrome.


## furl ##

This is an AppleScript snippet that prints the URL of the frontmost tab of the frontmost browser window ("furl" = "front URL"). I use the abbreviation `;furl` to invoke it.

The original version of this snippet (written for [TypeIt4Me][6]) is described [here][3]. I carried it along when I switched to TextExpander, then generalized it to handle both Chrome and Safari [here][4].

## 1url – 6url ##

These are AppleScript snippets that print the URL of the *n*th tab, counting from the left, of the frontmost browser window. I use the abbreviations `;1url` through `;6url` to invoke them.

These expansions of `;furl` were first described [here][5] and generalized to work with Chrome and Safari [here][4].

## surl ##

This is an AppleScript snippet that prints the shortened URL of the frontmost tab of the frontmost browser window ("surl" = "shortened URL"). It uses the [Metamark][10] shortening API, which requires special characters in the input URL to be encoded. The `escapeurl` script, included in the repository, is called by snippet to do the encoding. I use the abbreviation `;surl` to invoke it.

Like `;furl` this was first written for TypeIt4Me and described [here][3], then generalized to work with Chrome and Safari [here][4].

## 1surl – 6surl ##

These are AppleScript snippets that print the shortened URLs of the *n*th tab, counting from the left, of the frontmost browser window. It uses the [Metamark][10] shortening API, which requires special characters in the input URL to be encoded. The `escapeurl` script, included in the repository, is called by snippet to do the encoding. I use the abbreviations `;1surl` through `;6surl` to invoke them.

These snippets were first described [here][4].

## psurl ##

This is an AppleScript snippet that prints the shortened URL of the frontmost tab of the frontmost browser window in parentheses. It uses the [Metamark][10] shortening API, which requires special characters in the input URL to be encoded. The `escapeurl` script, included in the repository, is called by snippet to do the encoding. I use the abbreviation `(;surl` to invoke it.

This snippet was born out of frustration. I often put shortened URLs in parentheses in tweets, and I found myself—because TextExpander insisted on it—invoking `;surl` and then going back to put in the parentheses. This snippet made thing go much faster.

This snippet was first described [here][4].

## flickr ##

This is a shell script snippet written in Python/appscript. It prints the "flic.kr" shortened URL for the Flickr photo in the frontmost tab of the frontmost browser window. I use the abbreviation `;flickr` to invoke it.

This snippet was first described [here][7].

## 500 ##

This is a shell script snippet written in Python/appscript. It prints the URL of the smaller medium-sized version (the one that's 500 pixels wide if landscape) of the Flickr photo in frontmost tab of the frontmost browser window. I use the abbreviation `;500` to invoke it.

This snippet was first described [here][8], then improved to handle more Flickr pages [here][9].



[1]: http://appscript.sourceforge.net/index.html
[2]: http://smilesoftware.com/TextExpander/
[3]: http://www.leancrew.com/all-this/2008/03/long-and-shortened-urls-with-typeit4me/
[4]: http://www.leancrew.com/all-this/2010/10/textexpander-snippets-for-google-chrome/
[5]: http://www.leancrew.com/all-this/2009/07/safari-tab-urls-via-textexpander/
[6]: http://www.ettoresoftware.com/products/typeit4me/
[7]: http://www.leancrew.com/all-this/2010/03/shortened-flickr-urls/
[8]: http://www.leancrew.com/all-this/2010/07/flickr-image-url-via-textexpander/
[9]: http://www.leancrew.com/all-this/2010/07/updated-flickr-url-script-for-textexpander/
[10]: http://metamark.net/
