+++
author = "Alexandros"
categories = ["Linux"]
date = 2021-06-20T21:00:00Z
description = "How to be an exclusive terminal user"
featuredImage = "/images/zueyl-nt1x.jpg"
featuredImagePreview = ""
hiddenFromHomePage = false
hiddenFromSearch = false
lightgallery = false
tags = ["rss", "productivity", "linux"]
title = "How to live your digital life in a terminal : Introduction"

+++
# The bloated web

I recall a few years ago me sharing Mozilla’s dream for the web. The web was on its way to become the main platform for internet users. And that was supposed to be a good thing, due to its openness and the freedom that it was providing. But freedom and control are relative concepts.

Web now has become bloated with unnecessary code, advertisements, pop-ups, comments and recommendation systems that are trying to mine our data and keep us hooked in their user interfaces by providing us with constants hits of dopamine.

Is there a solution to this? Is there a way to get back our control and attention? Well, you could go off the grid. Or you could live your digital life in your computer's terminal. Living in the terminal means avoiding using applications with a graphical user interface (GUI). Or at least a good subset of them.
In this article, we will discuss some first steps to entry this life-style.

# RSS is still alive

RSS (Really Simple Syndication) is a web feed that allows users and applications to access updates to websites. It was released in March 1999 for use on the My.Netscape.Com portal. For a significant period, I believed it was dead. Fortunately, it recently received some traction.

My terminal workflow is based on RSS. RSS enables me to receive updates from blogs, news sites, Twitter, Reddit, YouTube channels and podcasts. My RSS client of choice is [newsboat](https://newsboat.org/). My OS of choice is Linux (Ubuntu or Arch Linux). The main thing you should know about configuring newsboat is you have to add your list of RSS feeds at `~/.newsboat/urls`. You can find plenty of useful information at the [Arch wiki](https://wiki.archlinux.org/index.php/Newsboat).

To receive RSS updates from a YouTube channel, add to your list: `http://www.youtube.com/feeds/videos.xml?channel_id=$channel_id`, where $channel_id is the id of the requested channel. Following Reddit updates is easy. In most cases, you can create an RSS feed by adding ".rss" to the end of an existing Reddit URL: http://www.reddit.com/.rss  
Twitter does not support RSS feeds, but you can generate one with the help of nitter: https://nitter.42l.fr/username/rss (also, do follow [me](https://nitter.42l.fr/ck0d3r/rss) please :P).

Newsboat also allows specifying the application which will open the videos/articles in the feeds. For example, you can use VLC to view YouTube videos, and Firefox to open website links. You can add the following line to your ~/.newsboat/config file:  
`macro y set browser "vlc %u" ; open-in-browser ; set browser "firefox %u"`

Although you cannot avoid using a GUI to enjoy Youtube, this setup is a magnitude more minimal. You avoid the ads, the annoying comments, the JavaScript tracking and the recommended/related videos. You can also play podcast episodes with the excellent [moc player](http://moc.daper.net). Now let’s talk about the trickiest component of this setup: the Web Browser.

There is a fair amount of command-line browsers out there. There is links, elinks, w3m, lynx and others. My personal favourite is w3m with image support. As you can guess, you can configure newsboat to open links with w3m. However, reading articles with w3m is not always piece of cake. A trick is to use [readability-cli](https://www.npmjs.com/package/readability-cli) to remove the bloat and keep only text related to the article’s content. You can easily combine readability with W3M :
`readable $url | w3m -T text/html`
For integration with newsboat, add this to the config file:
`macro r set browser "readable %u | w3m -T text/html" ; open-in-browser ; set browser "firefox %u"`.

# This is only the beginning

Undoubtedly RSS is a powerful tool that serves a minimalistic digital life. However, choosing RSS is only the first step.
There is a plethora of command-line tools that can empower us with more focused, private and productive digital lives.
There is a movement (mostly in the open-source community) that argues that the web has lost its initial vision and purpose.
Thus, the web protocol (HTTP) shall instead be replaced by a simpler/lighter alternative, with the main protagonist being [Gemini](https://gemini.circumlunar.space/); a protocol lighter than HTTP but heavier than the older [Gopher](https://web.cortland.edu/flteach/methods/obj1/gopher.html).