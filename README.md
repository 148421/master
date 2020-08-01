# DiscordBot
A chat bot for Discord app based off <a href="https://github.com/hydrabolt/discord.js/">discord.js</a>.

# Features:
- !gif query => returns a gif connected to search query. Example = !gif dogs
- !image query => returns an image from Google Images (careful, no adult filter) Example: !image dogs
- !youtube query=> returns a youtube link. Example: !youtube Fortnite
- !wiki query=> returns the summary of the first search result on Wikipedia. Example: Linus Torvalds
- !wolfram query => queries Wolfram Alpha for results
- !meme memetype "text1" "text2" => returns a meme image. notice the quotes around text, they are vitally important
- !say text => echos text
- !alias => create custom shorthand commands in channel!
- !join-server => bot will join the requested server
- !talk => talk with the bot!
- @botname => responds when @mentioned
- channel management!

And much more! Try `!help` to get a full list of available commands

# Installation

This bot is written to run on top of node.js. Please see https://nodejs.org/en/download/

Once you have NodeJS installed, running `npm install` from the bot directory should install all required packages. If this command prints errors, the bot won't work!



## Windows Users
Please note that you must have a working C compiler and Python in your path for
`npm install` to work. The bot has been tested to work on Windows using Visual Studio 2015 Community and Python 2.7, except for `!pullanddeploy`.
* [Installing Node on Windows](http://blog.teamtreehouse.com/install-node-js-npm-windows)
* [npm errors on Windows](http://stackoverflow.com/questions/21365714/nodejs-error-installing-with-npm)
* [Visual Studio Community 2015](https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx)
* [Python 2.7](https://www.python.org/downloads/)

[Tuck 64 was kind enough to make a video walkthrough of the setup process](https://www.youtube.com/watch?v=H-82S2jFOII)

## RSS
You can create an rss.json file adding rss feeds as commands. See rss.json.example for details.

## Special instructions for setting up google search and youtube APIs:

(thanks -Mango#7777)

1) Create a Custom Search at: https://cse.google.com/cse/create/new

2) Leave the first line blank, and name the search engine anything you wish.

3) Click "Advanced Options" and then type ImageObject.

4) Hit create.

5) On this new page, enable the Image Search in the menu.

6) Then press "Search engine ID" under the Details header.

7) Copy this into the auth.json's "google_custom_search" section.

Make sure you also have your Google server API key, which is located in the "youtube_api_key" section, or the search will fail.

# Running
Before the first run you will need to create an `auth.json` file. A bot token or the email and password for a discord account are required. The other credentials are not required for the bot to run, but they are highly recommended as commands that depend on them will malfunction. See `auth.json.example`.

To start the bot just run
`node discord_bot.js`.

# FAQ
1) Music is always saying "invalid video"
you likely need to update youtube-dl. you can do so with `node ./node_modules/youtube-dl/scripts/download.js`

# Updates
If you update the bot, please run `npm update` before starting it again. If you have
issues with this, you can try deleting your node_modules folder and then running
`npm install` again. Please see [Installation](#Installation).

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Feel free to create a fork and use the code.
