---
label: Installing Gotty
order: 100
icon: server
---

# How to Run Gotty on My Server?

GoTTY is a simple command line tool that turns your CLI tools into web applications. This guide will show you how to install and run GoTTY on your server.

## Installation and Setup

First, copy and run this command:

```bash
# Get the latest release.
curl -Lo gotty.tar.gz "https://github.com/yudai/gotty/releases/download/v1.0.1/gotty_linux_amd64.tar.gz"

# Extract the files.
tar -xvf gotty.tar.gz

# Run.
./gotty -w -c "user:password" -p "INSERT_PORT_HERE" bash
```

## Configuration Steps

1. Go to your server, then paste the script and remove `` ` `` if it is there.
2. Add your user and password but don't remove `:`, as this is needed.
3. Add your port number which can be found on the main page of your server.
4. Run it and enjoy!

## Example

```bash
./gotty -w -c "myuser:mypassword" -p "8080" bash
```

This will start GoTTY on port 8080 with the username `myuser` and password `mypassword`.

## References

- [GoTTY GitHub Repository](https://github.com/yudai/gotty)
- [GoTTY Releases](https://github.com/yudai/gotty/releases)

!!!info Last Updated:
December 24, 2025.
!!!