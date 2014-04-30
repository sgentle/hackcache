Hackcache
=========

This is a simple proof of concept showing how the HTML5 application cache can be
used to make an existing website defacement persistent for people who have
visited the site, even after the original server is fixed.

If you serve the contents of the goodserver directory (`cd goodserver && python
-m SimpleHTTPServer`), you should see an innocuous cat picture.

If you serve the contents of the badserver directory (`cd badserver && python -m
SimpleHTTPServer`), you will see an alternate page, simulating the kind of
hard-hitting political commentary you might experience on a defaced website.

Now go back and serve the goodserver directory again, simulating a wipe and
restore of the server.

On Firefox, you will still see the defaced page. Refreshing will not clear it,
you have to go into your settings and clear the app cache manually.

In Chrome and Safari, you will only see the defaced page once; refreshing will
display the correct site. However, you can work around this by naming the
application cache something that will still be on the server when it's cleaned.
badserver2 has an example of that using robots.txt.
