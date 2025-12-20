---
order: 40
icon: globe
---

# How to Proxy a Minecraft Server

If you want to access your Minecraft server using a custom domain (e.g., `play.yourdomain.com`) without requiring users to type in a port number, you can do so using **SRV Records**.

---

## Prerequisites

* A running Minecraft server on DBH.
* A custom domain managed via **Cloudflare** (recommended) or a domain registrar that supports **SRV Records**.
* Your server's **Port** and **Node Address** (e.g., `dono-02.danbot.host`).

---

## Setting up the SRV Record

Follow these steps to create the record in your DNS dashboard.

### Record Details

[!table-list]
* **Type:** `SRV`
* **Name:** Your subdomain (e.g., `play` for `play.yourdomain.com`)
* **Service:** `_minecraft`
* **Protocol:** See the tabs below (TCP vs UDP)
* **TTL:** `Auto`
* **Priority:** `0`
* **Weight:** `0`
* **Port:** Your unique DBH server port
* **Target:** The node address (e.g., `dono-02.danbot.host` or `dono-04.danbot.host`)

### Protocol Requirements
=== Java Edition
For Java Edition players, you must use the **TCP** protocol.
```text
Protocol: TCP
```
===
=== Bedrock Edition
Bedrock Edition For Bedrock/Pocket Edition players, you must use the UDP protocol.
```
Protocol: UDP
```