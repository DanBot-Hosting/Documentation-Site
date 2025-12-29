---
order: 60
icon: file-media
title: Installing Zipline
---

# Setting up a Zipline Server

[Zipline](https://zipline.diced.sh/) is a high-performance ShareX/file-upload server used to share screenshots and store files online.

---

## Prerequisites

* An **All in One Server (AIO)**
* A **Postgres 16** Server

---

## 1. Installation

On your AIO server, execute the following commands in the terminal:

```bash
# Clone the repository
git clone [https://github.com/diced/zipline](https://github.com/diced/zipline)
cd zipline

# Create a temporary directory for the installation
mkdir /home/container/tmp && export TMPDIR=/home/container/tmp

# Install dependencies
yarn install
```

## 2. Configuration

1. In your file explorer, navigate to the `/zipline/` folder.
2. Rename `env.local.example` to `env.local`.
3. Open `env.local` and apply the following recommended settings:

```env
CORE_RETURN_HTTPS=true # Set to false if you encounter SSL issues or use the default node domain.
CORE_SECRET="<random characters>"
CORE_PORT=<port of the aio server>
CORE_DATABASE_URL="postgres://pterodactyl:<db_password>@<db_ip>:<db_port>/zip10"
```

## 3. Starting the Server

Run the following commands:
```
# This builds the modules so it loads faster when you visit the site.
yarn build

# This starts the production server and runs on the settings you configured before.
yarn start
```
The server should now start and you can go to the aio server's IP + Port to log into to zipline. The default login is administrator/password. Once in the panel, click your username on the top right corner and select manage account. From here you can scroll down and generate the sharex config, which you can use to easily add this server to your client.

!!!
Make sure both servers are running when going through this process.
!!!

!!!
Thank you to raspi_dude (1005607106596057149) for creating this guide on the support channel.
!!!

!!!info Last Updated:
December 24, 2025.
!!!