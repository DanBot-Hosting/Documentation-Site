---
icon: file
---

# MongoDB

[MongoDB](https://www.mongodb.com/) is a source-available cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with optional schemas. MongoDB is developed by MongoDB Inc. and licensed under the Server Side Public License (SSPL).

[Source: Wikipedia](https://en.wikipedia.org/wiki/MongoDB)

# Creating the server

To create a server, we suppose that you've already [created and linked an account into the panel](/getting-started).

In that case, go to DBH server and run this command:

For a free server:

```
DBH!server create mongodb [optional server name]
```

For a donator server:

```
DBH!server create-donator mongodb [optional server name]
```

# Connect to the database

In order to connect to your fresh created database start the server and use the following link:

```text
mongodb://admin:password@nX.danbot.host:port/?authSource=admin
```

## Fields

The link given above isn't enough for you to connect to the database, now you have to modify it to actually connect to the database.

### Password

"password" can be found in the `Startup` tab.

![Password Location](/media/server-types/mongodb/password.png)

!!!
Given page screenshot is an example of the password, it does not carry any important information as the server was already deleted.
!!!

### Port

"port" is your server's port that can be found in the main page.

## Final result

As soon as you finished with the link it should look like this:

```text
mongodb://admin:81OCNEWWJZ1KA0TJ@pnode2.danbot.host:9608/?authSource=admin
```

# Conclusion

Now you can deal with NoSQL database. To find out more about mongodb visit their documentation website!

[MongoDB Docs](https://www.mongodb.com/docs/)

---

!!!info Last Updated:
December 27, 2025.
!!!