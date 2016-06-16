# \<twitter-widgets\>

#### Simple Polymer wrapper to load Twitter embed widgets on a local DOM.

`bower install --save joaovieira/twitter-widgets`

----

`twitter-widgets` is a simple wrapper for Twitter's embedded widgets (https://dev.twitter.com/web).

When using the native Shadow DOM, Twitter's library can't access widget's anchors within
your app component's local DOM.

This element loads Twitter's _widgets.js_ library asynchronously (https://dev.twitter.com/web/javascript/loading)
and tells it to look for widgets within its local DOM.

Example:

    <twitter-widgets>
      <a class="twitter-timeline" href="https://twitter.com/joaomgvieira">Tweets by joaomgvieira</a>
    </twitter-widgets>

Within `twitter-widgets` use the widget's anchor data attributes and classes as you would normally would.

Example:

    <twitter-widgets>
      <a class="twitter-timeline"
         height="500"
         data-tweet-limit="5"
         data-chrome="nofooter transparent"
         href="https://twitter.com/joaomgvieira">
       Tweets by joaomgvieira
     </a>
    </twitter-widgets>

** Note: `twitter-widgets` loads Twitter's widgets.js so you don't have to. Since it checks if the library
has already been loaded, it's safe to use this element multiple times on the same app/page.
For more information, see https://dev.twitter.com/web/javascript.
