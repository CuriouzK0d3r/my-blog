+++
author = "Alexandros"
categories = ["Linux"]
date = 2021-06-30T21:00:00Z
description = "Using social media tools from the terminal"
featuredImage = "/images/social.jpg"
featuredImagePreview = ""
hiddenFromHomePage = false
hiddenFromSearch = false
lightgallery = false
tags = ["linux", "productivity", "social-media"]
title = "How to be social in the terminal"

+++
## Online social networks

Whoever knows me personally is aware that I am not the biggest fan of social networks. Don't get me wrong, I was always involved with them. Understanding social networks was also part of my research interests for a quite long time. But my relationship with them was always a love and hate one.

In this blog, I'm going to talk a lot about this relationship.

In this post, though I will diverge from this discussion.

If you followed through with my last post, you may wonder what else is it possible to do from a command-line interface a.k.a. the terminal.

Wouldn’t it be nice to maintain a normal online social life while embracing minimalistic digital habits? Let's assume that you are a user of Reddit, Twitter, Instagram, Facebook Messenger, LinkedIn, Telegram, Slack and Discord. Although this is not the most convenient way to access those services, we will explore tools that make chatting and browsing possible.

Disclaimer: You shouldn’t normally trust your credentials to a third party service. I performed a manual check at the code of the suggested tools. They look legitimate. You should do your research though.

## Chatting with WeeChat

[WeeChat](https://weechat.org/) is an extensive chat client that includes an interesting list of plugins. Some plugins add features like proxy support, while others add support to social services, thus being worth mentioning. WeeChat can easily be combined with BitlBee, and bring support to additional services (Twitter/Discord/Steam). I used the Skype plugin in the past but now is outdated and not functional.

As far as the aforementioned services are concerned, I suggest WeeChat for its Slack and Discord integrations.

### Slack

[Wee-Slack](https://github.com/wee-slack/wee-slack) is a WeeChat plugin that is based on python WebSockets and delivers most of the basic functionality of the Slack client. To use this, you need to receive a Slack API token. One way is - after installing - to run on WeeChat:

`/slack register` This command prints a link you should open in your browser to authorize WeeChat with Slack.

Once you’ve accomplished this, you should run:

`/slack register <code>`

`/python reload slack`

Now you can navigate through private messages and channels using the arrow keys.

### Discord

To be honest, I am a fan of the excellent [cordless](https://github.com/Bios-Marcel/cordless) application. Unfortunately, the creator was banned from the service for violating the terms of service. So it is not recommended anymore.

An alternative however to this is a [WeeChat plugin](https://github.com/terminal-discord/weechat-discord).

Once more,  you will need to obtain a login token. You can either use a python script to find the tokens or try and grab them manually.

Then, set your token: `/discord token 123456789ABCDEF`

And connect: `/discord connect`

Then you can browse your channels and chat normally.

## Chatting with other tools

### Facebook Messenger

While WeeChat is a powerful enough tool, it serves our purpose up to a certain extend. To use Facebook messenger, will have 2 options:

- [fb-messenger-cli](https://www.npmjs.com/package/fb-messenger-cli)

- [Messer](https://github.com/mjkaufer/Messer)

I had some issues logging in with Messer, so I ended up using the first option.

I suggest installing the tool locally with npm.

To run this:

`> ./node_modules/fb-messenger-cli/cli.js # run the app`

`> 0 # choose a conversation`

`> this is a test message # text a message!`

### Telegram

In this case, we are lucky. We have a well-supported CLI application, [telegram-cli](https://github.com/vysheng/tg).

To try this, after installing, run:

`> telegram-cli # run the app!`

`> help # see your options`

`> msg username this is my test message # message user with the username handle!`

### Instagram DMs

Instagram is of course a tricky case because relies on images. However, we can still chat with [igdm-cli](https://github.com/mathdroid/igdm-cli).  To try this:

`> igdm # enter username and password`

`> # browse messages with arrows and enter`

`> # In chatroom mode, exit by entering '/end'. Manually refresh the room by entering '/refresh'.`

## Browsing and posting

As you can imagine, posting and browsing is a bit more problematic than messaging. Fortunately, there are some decent solutions, especially for Reddit and Twitter.

### Twitter

[Rainbowstream](https://github.com/orakaro/rainbowstream) is my favourite of the clients I have mentioned here. It is feature-rich, and enables a decent use of Twitter without being as distracting as the official clients.

After installing Rainbowstream, run:

`> rainbowstream # supports tab autocompletion`

`> h # for help`

`> h discover # help for more specific commands`

`> notification discover # shows notification`

`> home discover # shows timeline`

`> conversation [tweet id] # displays the full thread for tweet with the speicific id`

`> t testing rainbowstream # will tweet "testing rainbowstream"`

### Reddit

[Rtv] is a Reddit client that helps you to search and read posts and comments, while also gives you the ability to post and comment. Rtv also works as expected. To try this:

`> rtv`

`> /front # frontpage`

`> /u/me # your info`

`> /r/greece # visit the /r/greece subreddit`

### LinkedIn

With [linkedin-cli](https://pypi.org/project/linkedin-cli/), you can post on your feed with a few easy steps. You have to register an application and retrieve a client id and secret. Then:

`> linkedin configure set application # provide your client id and secret of your linkedin application. Configuration will be saved to ~/.linkedin/config.json file`

`> linkedin login # provide your credentials`

`> linkedin post -v public "Hello world!" # post with public visibility`

## Instagram

[instagram-terminal-news-feed](https://github.com/instagrambot/instagram-terminal-news-feed) is a promising Instagram client, that even enables displaying pictures on the terminal. Unfortunately, due to some error, I wasn't able to log in. If you manage to use this, ping me :).

## Bonus: Google search

Now I will admit that I cheated twice. First, because Google search is not a social network, and second because I wouldn't suggest using Google search even from the command line.

I know, we all use it. But DuckDuckGo is a more private alternative. Thus, I will recommend a tool for performing duckduckgo searches from the terminal.

[Ddgr](https://github.com/jarun/ddgr) is a cmd line utility to search DuckDuckGo (HTML version) from the terminal. Although there is a Google alternative (googler), It is unmaintained and does not work anymore.

You can easily use ddgr and also specify the cmd line browser of your choice:

`BROWSER=w3m ddgr query`

This tool supports many options, and I think you will enjoy using it.