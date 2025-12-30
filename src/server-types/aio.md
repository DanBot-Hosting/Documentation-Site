---
icon: file
---

# All In One (AIO)

`All In One` is a unique server type that contains several features that distinguish it from other Development (Bot & Codeserver) server types. This type brings all of the other types into a single server type and lets users interact with console.

---

## Requirements

- Have an account created and linked to the panel. [Click here if you have not done so already.](/getting-started)

---

## Creating the server

To create a free server, go into `#⌛╏commands` and run `DBH!server create aio [optional server name]` to create a free server. Once you have done so, the bot should return the following output.

If you are creating a donator server, instead run `DBH!server create-donator aio [optional server name]` 

---

## Startup

In the `Startup` tab, you might find out the startup command is `bash`. This lets you interact with unix-like OS commands, git, npm, py, java etc. up until you "launch" the server e.g., `node .`.

---

## Bash

To make starting your code easier, you can change the startup command to `bash start.sh` if you have a start.sh file to start your code. If you are using something like nodejs on an AIO server, all you have to do is change the startup command to `node .`.

Please note that if you do change the startup command from `bash`, you will lose the ability to run commands in the console.

!!!info Last Updated:
December 30, 2025.
!!!