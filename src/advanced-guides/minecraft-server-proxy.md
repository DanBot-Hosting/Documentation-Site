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

Field | Value | Description
:--- | :---: | ---:
**Type** | `SRV` | The DNS record type
**Name** | Your subdomain | e.g., `play` for `play.yourdomain.com`
**Service** | `_minecraft` | The service identifier
**Protocol** | TCP or UDP | See the tabs below (TCP vs UDP)
**TTL** | `Auto` | Time to live
**Priority** | `0` | Priority value
**Weight** | `0` | Weight value
**Port** | Your server port | Your unique DBH server port
**Target** | Node address | e.g., `dono-02.danbot.host` or `dono-04.danbot.host`

---
### Example:

![Example from Cloudflare|600x400](/media/minecraft-server-proxy-cloudflare.png)

---
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
===

!!!info Last Updated:
December 24, 2025.
!!!