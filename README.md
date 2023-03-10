# MagpieTutor
Scryfall bot but for IMF

## How to host the bot yourself
If you know how to set up a discord bot with discord.js already, then download all the package with `npm setup`, then created a `config.json` with these information: 
```json
{
    "clientId": "Your Client ID here",
    "token": "Your Bot Token here",
}
```
And running `npm start` should start the bot

If you don't know how to setup a discord bot follow these step:
1. Download [Node](https://nodejs.org/en/)
2. Go to the [Discord Developer Portal](https://discord.com/developers/applications)
3. Click on `New Application` in the top right. Give the Application a name (This is not the name of your bot but it recommend to make it the same or similar name as your bot), accept the TOS and create it.
4. Click on the `Bot` menu and choose `Add Bot`, you can change the name of the bot if you want here.
5. Click the `Copy` button below `Token`.
6. Click on the `OAuth2` menu and choose `URL Generator` choose `bot` and `application.commands` option.
7. In the `Bot Permission` section and choose `Administrator`. Now you can click `Copy` at the very bottom to get the bot.invite link. **You have to invite the bot to a server for future step**.
8. Now download this repository, unzip the folder if it a zip file.
9. Make a `config.json` file, in there type the following: 
```json
{
    "clientId": "Your Client ID here",
    "token": "Your Bot Token here",
}
```
10. You can put the token that you copy and replace the text `Your Bot Token here`
11. Go into your discord client `Setting` > `Advance` and turn on `Developer Mode`
12. You can now copy the bot client ID by right clicking and select `Copy ID`. You can replace the text `Your Client ID here` in `config.json` with this ID. Save the file if you haven't already. 
13. Right click and choose `Open in Terminal` option or go to the path text box and type in `cmd`.
14. Run the command `npm setup` to install all the necessary packet for the bot and install the commands.
15. Finally run `npm start` to host the bot.

If you have any problem ask me on Discord my DM should be open. `Stoat#3922`

## Commands

### Draft Command
Draft a deck from opening Pack

#### Argument
- `set`: Which set you want to draft from (You cannot choose multiple set)
- `size`: The final deck side or how many pack you want to open
- Option for excluding certain cost. Free card will still appear:
    - `beast`: Remove all cards that cost blood from the draft pool
    - `undead`: Remove all cards that cost blood from the draft pool
    - `tech`: Remove all cards that cost blood from the draft pool
    - `magick`: Remove all cards that cost blood from the draft pool. This will also remove all the cards that support magick
  
#### Note
- You cannot undo selection. 
- Once you have 4 of the same common and try to take a fifth you will receive a Wild instead 
- Wild can be use to trade in any common card
- Once you exhaust the list of rare in the draft pool you will not get any more rare

### Set Code Command
Show the set code that you can use to search

Current set code:
- c: competitive
- e: eternal
- v: vanilla
- m: magic the gathering

### Deck Sim Command
Simulate deck draw for whatever reason

#### Argument
- `deck-file`: The deck file you want to simulate
- `deck-list`: The deck list you want to simulate. Card separate by commas (",")
- `detail`: Show more detail about the deck like card draw percentage, which card are left, etc

#### Note
- Select `End` if you stop using it

### Tunnel Status Command
Current Status of tunnel

### Color Text Command
Generate a color text thing for discord

#### Color Tag
- $$g: Make the text after this tag gray
- $$r: Make the text after this tag red
- $$e: Make the text after this tag green
- $$y: Make the text after this tag yellow
- $$b: Make the text after this tag blue
- $$p: Make the text after this tag pink
- $$c: Make the text after this tag cyan
- $$w: Make the text after this tag white

- $$1: Make the background of the text after this tag Firefly Dark Blue
- $$2: Make the background of the text after this tag Orange
- $$3: Make the background of the text after this tag Marble Blue
- $$4: Make the background of the text after this tag Greyish Turquoise
- $$5: Make the background of the text after this tag Gray
- $$6: Make the background of the text after this tag Indigo
- $$7: Make the background of the text after this tag Light Gray
- $$8: Make the background of the text after this tag White

- $$l: Bold the text after this tag
- $$u: Underline the text after this tag

- $$0: Reset everything

#### Note
If you want to see what the color look like or how this command work in the background check out this [guide](https://gist.github.com/kkrypt0nn/a02506f3712ff2d1c8ca7c9e0aed7c06)

### Guess the Card Command
Magpie will send you part of a card and you need to guess the card