---
label: MariaDB Setup for WordPress
order: -5
icon: server
---

# Setting up MariaDB Egg for WordPress

This guide will help you configure a MariaDB database for your WordPress installation.

## About the Technologies

**WordPress** is a free and open-source content management system (CMS) written in PHP. It's one of the most popular website creation tools, powering over 40% of all websites on the internet.

**MariaDB** is a community-developed, commercially supported fork of the MySQL relational database management system. It's designed to be highly compatible with MySQL while offering additional features and improved performance.

## Database Setup Commands

Run the following SQL commands in your MariaDB console to set up the database for WordPress:

```sql
CREATE DATABASE wordpress;

CREATE USER "your_username"@"your_allowed_ipaddr" IDENTIFIED BY "your_password";

GRANT ALL PRIVILEGES ON wordpress.* TO "your_username"@"your_allowed_ipaddr";

FLUSH PRIVILEGES;
```

## Configuration Notes

### Port Configuration

Make sure to change your `port` in `.my.cnf` to your server port, including the double ticks when executing the command.

### IP Address Configuration

Please note that `your_allowed_ipaddr` is the IP of the node that your WordPress is hosted on. If it's on the same node, use Docker local IP `172.17.0.1`.

## Example Configuration

```sql
CREATE DATABASE wordpress;

CREATE USER "wpuser"@"172.17.0.1" IDENTIFIED BY "SecurePassword123";

GRANT ALL PRIVILEGES ON wordpress.* TO "wpuser"@"172.17.0.1";

FLUSH PRIVILEGES;
```

## References

- [WordPress Official Website](https://wordpress.org/)
- [MariaDB Official Documentation](https://mariadb.org/documentation/)
- [WordPress Database Configuration](https://wordpress.org/support/article/creating-database-for-wordpress/)
- [MariaDB User Management](https://mariadb.com/kb/en/create-user/)

!!!info Last Updated:
December 24, 2025.
!!!