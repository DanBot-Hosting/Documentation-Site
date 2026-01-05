---
icon: file
---

# Gitea

Gitea is an open-source forge software package for hosting software development version control using Git as well as other collaborative features like bug tracking, wikis and code review. It supports self-hosting but also provides a free public first-party instance.

!!!
It is important to thoroughly read and follow this guide, as one mistake might end up in you having to recreate the server.
!!!

!!!
This guide is not fully completed yet. If you don't know what you're doing, then wait until the guide is completed.
!!!

---

## Requirements

- Have an account created and linked to the panel. [Click here if you have not done so already.](/getting-started)

---

## Creating the server

To create a free server, go into `#⌛╏commands` and run `DBH!server create gitea [optional server name]` to create a free server. Once you have done so, the bot should return the following output.

```
Server Successfully Created
Click Here to Access Your Server
Status:    User ID:    Type:
Created    16464       gitea
Server Name:
Untitled Server (settings -> server name)
```

If you are creating a donator server, instead run `DBH!server create-donator gitea [optional server name]` 

---

## Configuration

Once the server has finished installing, go to files, then open the `custom` folder and finally open `app.ini`.

Gitea has an SSL bug, so your browser won't access the server via the server's default domain because the SSL certificate is broken. **We recommend proxying the domain.**
Now, edit the domain (just replace the 0.0.0.0) with your Proxied domain (if you have) or the server's default domain WITHOUT the port. Once done, the config should be something like this.

```ini
[server]
    LOCAL_ROOT_URL = http://0.0.0.0:7714/
    DOMAIN           = dono-XX.danbot.host
    HTTP_PORT        = 7714
    DISABLE_SSH      = true
    SSH_PORT         = 2020
```

---

## Creating a database

If you want to use a database on a different server, follow the guide for [PostgreSQL](/server-types/postgres) and note the node, password and port down as you'll need it for [the database settings.](#database-settings)

---

## Configuring the server

Now start the server. It may take a bit, so wait patiently.

Once it has started, open the site using the domain you put in the app.ini file with the server port.

Once done, you should be at the configuration page for Gitea.

You can close this page, but your configuration will not save until you finish it and click Install Gitea at the bottom of the page.

### Database settings

**Database Type:** Set it to which database you'll be using. In this case, PostgreSQL.

**Host:** Use the node and port your PostgreSQL server is on. Example: `dono-03.danbot.host:1234`

**Username:** Set it to pterodactyl.

**Password:** Use the password you noted down earlier. If you forgot it, click [here](/server-types/postgres/#password) and follow what it says to find it.

**Database Name:** Set it to postgres.

**SSL:** Leave it as default.

**Schema:** Leave it as default.

### General settings

**Site Title:** Leave it as default or give it a name.

**Repository Root Path, Git LFS Root Path & Run As Username:** LEAVE IT AS DEFAULT. It's your fault if you edit them and Gitea doesn't work.

**Server Domain:** If you set it up in `app.ini` you won't need to edit this.

**SSH Server Port:** Leave the box empty.

**Gitea HTTP Listen Port:** LEAVE IT AS DEFAULT.

**Gitea Base URL:** Leave it as default unless you are using a proxied domain. If you are, then remove the port.

**Log path:** Leave it as default.

### Optional settings

These settings will not be explained as thoroughly, but it is suggested to read this.

**Email settings**

This setting is not needed as Gitea is intended for private use, but if you want you can add an email server so you can get updates of your repositories.

**Server and Third-Party Service Settings**

Here you can set up Services that will work with Gitea. Hover your mouse over any option for more information.

**Administrator Account Settings**

You can add an admin account now to make it simpler, but if you don't, the first account created will be admin by default.

---

## Configuration & installation conclusion

After clicking "Install Gitea" you should be patient and **wait** until Gitea gets installed successfully. You can see the progress in the server's logs.

---

## 504 Gateway Time-out and 503 Bad Gateway

This is a very common error and may appear during installation. This is due to the server still installing and maybe rebooting. **DON'T RELOAD OR PRESS F5 AS YOU WILL START THE PROCESS AGAIN OR BREAK THE INSTALLATION.** To reload, just type the server's domain back in. **NEVER RELOAD.**

---

Once it has installed, you should be brought to the main page of Gitea. Once you are here, you can safely reload the web page without issue.

---

!!!info Last Updated:
December 27, 2025.
!!!