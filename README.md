gtasker
=======

**gtasker** is a web interface to put multiple Google Tasks windows side-by-side. You can configure it to display multiple rows and/or columns. How does it accomplish this magic? Iframes and a bit of JavaScript.

![GTasker Screenshot](./screenshots/gtasker-screenshot.png)

**gtasker** works as of April 2017 when it is locally hosted and viewed in Safari 10.1 on MacOS. More on that in a moment.

## Installation
1. Clone this repository to your local machine.
2. Open `index.html` in Safari on MacOS. (It is uncertain whether this will run in other browsers or on other OSes.)
3. Enjoy!

## Issues and Next Steps
The primary issue with gtasker as it is currently designed is that Google returns the HTTP Header `X-Frame-Options` (more on that [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)) with the Google Tasks page that prevents your task lists from being loaded in an HTML frame/iframe. Here is the full Google Chrome error:

```
Refused to display 'https://mail.google.com/tasks/ig?up_CurrentListId=' in a frame because it set 'X-Frame-Options' to 'sameorigin'.
```

The current workaround is to open gtasker from your local filesystem in Safari on MacOS. For some reason Safari allows the pages to render, but only when the gtasker page is hosted locally. It does not currently work when hosted from a web host in *either* Chrome or Safari, or when hosted locally in Chrome.

Next steps for anyone that would like to fork this:
* Find a workaround for the `X-Frame-Options` issue noted above.
* Remove the extraneous Wayback Machine code still present.
* Fix the occasional error where the Google Tasks interface renders about 15px too tall at first, but fixes itself upon screen resize.


## Credit / History
I'm glad to serve as a steward of **gtasker**, though I didn't originally create it, and the site and html file had no copyright, author/attribution or license.

*Update: Someone with a username *cmikec* may have created this (see this post on [Hacker News](https://news.ycombinator.com/item?id=2278860)).*

It was originally hosted at gtasker.com, but when that domain lapsed and the html+JavaScript was no longer available, I reconstituted it from the [Internet Archive Wayback Machine](https://archive.org/web/). I fixed some of the JavaScript that was broken, and then hosted it for a time on my own website [justinh.org](http://justinh.org).

When I stopped using gtasker in 2013, I posted it here to make it easy for people to download/fork it for themselves.

Read my two posts about it:
* [gtasker – reposting a great Google Tasks tool](http://justinh.org/2012/03/26/gtasker-reposting-a-great-google-tasks-tool/)
* [Fixing gtasker](http://justinh.org/2013/01/26/fixing-gtasker/)


Cheers!

-Justin  
i o {at} justin h (dot) org
