# r/place Nordic Union Bot (fork of PlaceNL)

The bot for the r/place Nordic Union and their allies! This bot connects with the [command server](https://github.com/PlaceNL/Commando) and gets its orders from there.

## User script bot

### Installation instructions

before you start, make sure your cooldown has run out!

1. Install the [Tampermonkey](https://www.tampermonkey.net/) browser extention.
2. Click on this link: [https://github.com/PlaceNordic/Bot/raw/master/placenlbot.user.js](https://github.com/PlaceNordic/Bot/raw/master/placenlbot.user.js). If everything went well you'll see Tampermonkey ask you to add it. Click **Install**.
3. Reload your **r/place** tab. If everything went well, you'll see "Getting access token..." in the top right of your screen. The bot is now active, You'll be able to see what the bot is doing through these messages.

### Cons of this bot

- When the bot places a pixel, it will look as if it wasn't placed, while the bot has already done that (and thus you're in cooldown). You can see the cooldown in the topright of your screen.

## Headless bot

### How to get reddit_session cookie

**NOTE: People have reported that this is annoying to do on chrome because teksts get unselected. Therefore we recommend that you use firefox.**

1. Go to [r/place](https://reddit.com/r/place)
2. Open dev tools and go to the network tab
3. Refresh the page
4. Click on the first request to reddit.com/r/place (See image)
   ![Screenshot_20220403_165251](https://user-images.githubusercontent.com/9784257/161433856-27ef7e7c-7f00-4b37-b274-4199ea919aa9.png)
5. Go to the tab called `Cookies`
6. Copy the value of the `reddit_session` cookie

### Installation instructions

1. Install [NodeJS](https://nodejs.org/).
2. Download the bot via [this link](https://github.com/PlaceNordic/Bot/archive/refs/heads/master.zip).
3. Extract the bot anywhere on your desktop
4. Open a command prompt/terminal in this folder
   Windows: Shift+right mousebutton in the folder -> Click on "open Powershell here"

   Mac: No clue, sorry!

   Linux: Is this necessary?

5. install the dependencies: `npm i`
6. execute the bot `node bot.js SESSION_COOKIE_HERE`
7. BONUS: You can repeat these steps for any amount of accounts you'd want. Keep in mind to use different accounts.

# Docker alternative

This option is mostly useful for people who are already using docker.

It has been confirmed to run on x64(average desktop computer) and armv7(raspberry pi), but it should also be able to run on arm64(new apple computers).

1. Install [Docker](https://docs.docker.com/get-docker/)
2. Run this command: `docker run --pull=always --restart unless-stopped -it ghcr.io/placenl/placenl-bot SESSION_COOKIE_HERE`

---
