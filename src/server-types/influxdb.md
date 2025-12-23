---
icon: file
---

# InfluxDB

[InfluxDB](https://www.influxdata.com/) is an open-source time series database (TSDB) developed by the company InfluxData. It is used for storage and retrieval of time series data in fields such as operations monitoring, application metrics, Internet of Things sensor data, and real-time analytics. It also has support for processing data from Graphite.

[Source: Wikipedia](https://en.wikipedia.org/wiki/InfluxDB)

# Creating the Server

To create a server, we suppose that you've already [created and linked an account into the panel](/getting-started).

In that case, go to DBH server and run this command:

For a free server:

```
DBH!server create influxdb [optional server name]
```

For a donator server:

```
DBH!server create-donator influxdb [optional server name]
```

# Get Database Online

1. On the server InfluxDB is running on, visit the server address (ex: http://pnode1.danbot.host:1234).
2. Click Get Started

## Set up your initial user

1. Enter a Username for your initial user.
2. Enter a Password and Confirm Password for your user.
3. Enter your initial Organization Name.
4. Enter your initial Bucket Name.
5. Click Continue.
6. Copy the provided operator API token and store it for safe keeping.

And now you have everything setup!

## Fields

The link given above isn't enough for you to connect to the database, now you have to modify it to actually connect to the database.

### Password

Your "password" is actually a API Token you should have created in the first step

### Port

"port" is your server's port that can be found in the main page.

# Conclusion

Now you can deal with NoSQL database. To find out more about InfluxDB visit their documentation website!

[InfluxDB Docs](https://docs.influxdata.com/influxdb/v2/)
