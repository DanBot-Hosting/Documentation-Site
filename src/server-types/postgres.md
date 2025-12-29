---
icon: file
---

# PostgreSQL

[PostgreSQL](https://www.postgresql.org/), also known as Postgres, is a free and open-source relational database management system emphasizing extensibility and SQL compliance. PostgreSQL features transactions with atomicity, consistency, isolation, durability properties, automatically updatable views, materialized views, triggers, foreign keys, and stored procedures.

---

## Requirements

- Have an account created and linked to the panel. [Click here if you have not done so already.](/getting-started)

---

## Creating the server

Here at DBH, we have two different versions of Postgres. We have Postgres14 and Postgres16. They are both relatively the same, but just a different version.

To create a free server, go into `#⌛╏commands` and run `DBH!server create (postgres14|postgres16) [optional server name]` to create a free server. Once you have done so, the bot should return the following output.

```
Server Successfully Created
Click Here to Access Your Server
Status:    User ID:    Type:
Created    16464       (postgres14|postgres16)
Server Name:
Untitled Server (settings -> server name)
```

If you are creating a donator server, instead run `DBH!server create-donator (postgres14|postgres16) [optional server name]` 

---

## Connecting to the database

In order to connect to your database, start the server and use the following connection string:
```
postgres://pterodactyl:<PASSWORD>@dono-XX.danbot.host:<port>/postgres
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

Your server's password can be found in the startup tab under the variable `Superuser Password`.

### Port

You must use your server's assigned port found on the main page after the node domain. Example: `dono-03.danbot.host:1234`

---

## Final result

Once you have finished modifying the connection string, it should look like this:

```
postgres://pterodactyl:th!s!snot-p-ssword@dono-03.danbot.host:1234/postgres
```