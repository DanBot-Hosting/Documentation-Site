---
order: 10
icon: rocket
---

# Getting Started

This guide provides a step-by-step tutorial on how to get started with DanBot Hosting (DBH). These instructions are mirrored from the `#📗╏getting-started` channel in our Discord Server.

[!ref target="beginner-guidebook" text="Check the Beginner's Guidebook for more details"]

---

### Step 1: Join the Discord Server
Joining the Discord server is essential because your panel account is managed via the [**@DanBot Hosting**](https://discord.com/users/640161047671603205) bot.

[!button variant="primary" text="Join DBH Discord Server" icon="link-external" target="https://discord.gg/dbh"]

---

### Step 2: Create your Panel Account
Head over to the [#⌛╏commands](https://discord.com/channels/639477525927690240/898041850890440725) channel and run the following command:

`DBH!user new`

The bot will create a private channel for you. Follow the instructions provided in that channel to finish setting up your account.

---

### Step 3: Link your Account
To ensure your Discord account and Panel account are synchronized, run:

`DBH!user link`

Follow the bot's instructions to complete the linking process.

---

### Step 4: Create your First Server
You can create your first server directly through the bot before logging into the [Web Panel](https://panel.danbot.host/).

**1. View available server types:**
`DBH!server create list`

**2. Create the server:**
`DBH!create server <type> <name>`

!!!secondary Note:
You can leave the server name blank if you haven't decided yet! You can change it later in the **Settings** tab on the panel.
!!!

---

## Managing your Server

### Deleting a Server
If you need to remove a server, use the following command:

`DBH!server delete <server_id>`

### How to find your Server ID
There are three ways to locate your unique Server ID:

1. **The Panel:** Go to the server's **Settings** tab in the [DBH Panel](https://panel.danbot.host/).
2. **Discord Command:** Type `DBH!server list` to view all your servers and their IDs.
3. **The URL:** Look at your browser address bar when viewing a server: `panel.danbot.host/server/`**`2c84d848`** (The last part is the ID).