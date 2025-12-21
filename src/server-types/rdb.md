---
icon: file
---

# RedDiscordBot (RDB)

Red Discord bot is a multi-modular Discord bot with a basic set of built-in commands. You can add more commands with cogs. It has over 550 available cogs, in addition to many default commands.

---

## Requirements

- Have an account created and linked to the panel. [Click here if you have not done so already.](/getting-started)

---

## Creating the server

To create a free server, go into `#⌛╏commands` and run `DBH!server create redbot [optional server name]` to create a free server. Once you have done so, the bot should return the following output.

```
Server Successfully Created
Click Here to Access Your Server
Status:    User ID:    Type:
Created    16464       redbot
Server Name:
Untitled Server (settings -> server name)
```

If you are creating a donator server, instead run `DBH!server create-donator redbot [optional server name]` 

---

## Configuration

---

### 1. Setup config.json

---

First, open your server, go to files, then navigate to `.config/Red-DiscordBot` and create a new config.json file with the following:

```json
{
    "pterodactyl": {
        "DATA_PATH": "/home/container/.local/share/Red-DiscordBot/data/pterodactyl",
        "COG_PATH_APPEND": "cogs",
        "CORE_PATH_APPEND": "core",
        "STORAGE_TYPE": "JSON",
        "STORAGE_DETAILS": {}
    }
}
```

---

### 2. Setup basic bot info

---

**Token**: Go to your server's startup tab. In variables there should be a DISCORD BOT TOKEN. In that field, remove all the text and paste your discord bot token.

**Prefix**: Go to your server's startup tab. In variables there should be a COMMAND PREFIX. In that field, remove everything and fill in your prefix.

For owner, you cannot just put your user ID in the owner variable. You instead need to add `--owner` to your prefix variable, then your user ID.

Example: `. --owner 569352110991343616`

`.` is my prefix, and `--owner 569352110991343616` defines my user ID is the bot owner. Replace it with your ID and your command prefix. For extra developer commands, you can also add `--dev` after your user ID.

Example: `. --owner 569352110991343616 --dev`