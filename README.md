static-ping
===========

Simple feed ping notifier for static sites (i.e.  Jekyll).
Currently supports Ping-O-Matic and PubSubHubbub.

### Setup & Install

1. Update the `$config` var in `ping.php` to match your site's information.
2. Make sure `ping.php` is deployed with your site to a publicly accessible URL.
2. Be sure to add the correct `hub` information to your RSS/Atom feed. (You can probably stick with Google's as in the examples below.)

For Atom:

    <feed xmlns="http://www.w3.org/2005/Atom">
      <link rel="hub" href="https://pubsubhubbub.appspot.com"/>
      ...
    </feed>


And for RSS:

    <rss xmlns:atom="http://www.w3.org/2005/Atom">
      <channel>
        <atom:link rel="hub" href="https://pubsubhubbub.appspot.com"/>
        ...
      </channel>
    </rss>

### Usage

Run the script. Either in a browser, or via your own code that makes an HTTP Get/Post call to it. For simplicity, setup a post-deploy script that triggers it when your site is deployed.
