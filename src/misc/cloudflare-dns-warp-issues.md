---
label: Cloudflare WARP Issues
icon: book
---

# What is Cloudflare WARP?

Cloudflare WARP is a combined DNS and VPN service provided by Cloudflare to run through their network.

[Site Link](https://one.one.one.one/)

---

## Why am I having issues connecting to DanBot Hosting?

Cloudflare WARP by sets the `.host` TLD as a local domain fallback automatically. That means it will try to request the DNS information from your local network.

This makes sense for intranets that have a `.host` domain as their intranet domain. The issue is it's a **public TLD**, so .host is also used on many internet facing sites, such as DanBot Hosting, specifically `danbot.host`.

## How do I fix it?

### 1. Open WARP Client:

![WARP Client](/media/cloudflare-warp/cloudflare-warp-1.png)

### 2. Click Settings/Gear Icon

![WARP Client](/media/cloudflare-warp/cloudflare-warp-2.png)

### 3. Click Advanced Section

![WARP Client](/media/cloudflare-warp/cloudflare-warp-3.png)

### 4. Click on Local Domain Fallback

![WARP Client](/media/cloudflare-warp/cloudflare-warp-4.png)

### 5. Select `host` and then click the delete/minus button:

![WARP Client](/media/cloudflare-warp/cloudflare-warp-5.png)

### 6. It should look like this:

![WARP Client](/media/cloudflare-warp/cloudflare-warp-6.png)

!!!info Info
Do note that removing `.host` will result in all .host to be resolved by external DNS and not local. This may or may not break your DNS setup.
!!!