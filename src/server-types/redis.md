---
icon: file
---

# Redis

[Redis](https://redis.io/) is a source-available, in-memory storage, used as a distributed, in-memory key–value database, cache, and message broker, with optional durability. Because it holds all data in memory and because of its design, Redis offers low-latency reads and writes, making it particularly suitable for use cases that require a cache. Redis is the most popular NoSQL database, and one of the most popular databases overall.

---

## Requirements

- Have an account created and linked to the panel. [Click here if you have not done so already.](/getting-started)

---

## Creating the server

To create a free server, go into `#⌛╏commands` and run `DBH!server create redis [optional server name]` to create a free server. Once you have done so, the bot should return the following output.

```
Server Successfully Created
Click Here to Access Your Server
Status:    User ID:    Type:
Created    16464       redis
Server Name:
Untitled Server (settings -> server name)
```

If you are creating a donator server, instead run `DBH!server create-donator redis [optional server name]` 

---

## Connecting to the database

In order to connect to your database, start the server and use the following connection string:
```
redis://default:<PASSWORD>@dono-XX.danbot.host:<port>
```

---

## Fields

The given connection string above will not be enough to connect to the database. Now you need to modify it to be able to connect.

### Node

Replace "dono-XX.danbot.host" with the server's node. Below is a table with the node domains.

| Free Node | Domain             |
| :-------- | :----------------- |
| PNode 1   | pnode1.danbot.host |

| Dono Node | Domain          |
| :-------- | :------------------ |
| Dono 01   | dono-01.danbot.host |
| Dono 03   | dono-03.danbot.host |

### Password

Your server's password can be found in the startup tab under the variable `Redis Password`.

### Port

You must use your server's assigned port found on the main page after the node domain. Example: `dono-03.danbot.host:1234`

---

## Final result

Once you have finished modifying the connection string, it should look like this:

```
redis://default:th!s!snot-p-ssword@dono-03.danbot.host:1234
```

---

!!!info Last Updated:
December 27, 2025.
!!!