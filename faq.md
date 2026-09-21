# DBH FAQ & Guides

List of common FAQ questions that have come up over the years.

---

## General
### How do I contact support?
Support is available via our ticket system at [billing.danbot.host](https://billing.danbot.host) via the ticket category. Make sure to place your ticket in the correct category, as different staff work on different sections.
### How long does it take for a support ticket to be responded to?
Depending on which category, a different staff member make take longer to respond due to the difficultly. Simple tickets should be processed within days, but response times will vary.
### Are suspension appeals handled via tickets?
No, suspension appeals are not handled via tickets. They are handled via our appeals email (`appeals@danbot.host`). Pelase see the [appeals guide for more information](/appealing-a-ban).

---

## Previous Nodes
### Where did Dono-02 and Dono-04 go?
All data for our servers were migrated to our new dedicated server in the US. However we are still navigating the current climate regarding resources to bring it up to full capacity. Game servers require sustained amounts of RAM to bring online, and we have no ETA on their return.
### Where did Performance Node 1 (PNode-1) go?
They were migrated over to our new server, however we are still navigating the current climate regarding resources. We have no ETA on their return. 

---

## Donations & Premium Servers
### How do I get donator servers? How do I donate? How do I get better servers?
  - Donate at https://paypal.me/DanBotHosting (minimum $1, priced at `$0.50` per premium server).
  - Include your Discord ID in the notes on the PayPal transaction.
  - Open a ticket via our billing panel and include both a screenshot of the transaction, the transaction ID, and the Discord ID. This allows our automated systems setup the donation to be single click approved by our staff.
### How long does it take for my donation to be processed?
It can take anywhere from 24 to 72 business hours to process from our systems. You must open a ticket to get such transactions processed. You can bump your ticket if it has exceed this time by sending a follow up message.
### Can I exchange my donations for credits on billing site?
Yes, you can. You must send proof of transaction that were made, as well as provide both Discord ID, Pterodactyl panel email, and billing panel email to process it via a ticket. It can go under Support / PayPal Transaction categories, and a staff member will process it once verified. This can take up to 72 business hours. You can bump your ticket if it has exceed this time by sending a follow up message.

---

## DBH VPN
### What is the expected price of DBH VPN?
Free, with paid add-ons such as static IPs and premium locations (currently in development).

---

## Common Issues: 
### "No Space" error even with free disk. How do I fix it?
Known issue from RAID setup on the new SSDs; being worked on.
### Out-of-space errors when installing packages. How do I fix it?
  - Installs use a tempporary (temp) directory limited to 100MB on the host. Packages larger than that limit fail with out-of-space messages.
  - For the container TMPDIR workaround, see: [Fixing `EnvironmentError - No space left on device`](/guides/fixing-no-space-temp).

---

## Hosting Support
### Do you support Lavalink servers?
Yes. Limit RAM to 2GB to prevent automated abuse detection systems from firing. Must be in good faith.
### Node IPs?
Provided on request; check the panel or ask staff if you need specifics. We recommend running simple ping command in terminal:

  ```
  ping dono-01.danbot.host
  ```

  Where Node information can be found on the server settings or the server address on the main page.
### Having issues with the DBH Pterodactyl API?
Set the user agent to `DBH` when calling the API.
### Proxied domains not using HTTPS:
Enable Force HTTPS by unproxying/reproxying or switching Cloudflare from DNS-only to Proxied (orange cloud), then in SSL enable "Always HTTPS."
  
---

## Providers
### What hosts do we use?
Primarily CrunchBits and BerryByte, followed by OVHCloud and a few colocated VPS hosts.

---

## Policies
### What are you not allowed to host?
See the full list [here](/policies/policy-list).
### What is the difference between Free Nodes and Donator Nodes?
Donator servers are paid and limited to donors or code claimers.
### What's the catch? Why is it free?
Started in 2016 to help friends test projects; it grew into a business and a learning platform for system administration. Using DBH helps it grow and supports ongoing learning. We do have limited resources but make the most out of it.
### Why don't we change startup commands for users?
Avoids false anti-abuse flags and prevents unstable startup flags from harming servers or nodes. This is non negotiable. 
### Why no additional allocations for servers?
Allocations control server counts; extra allocations would skew usage data.
### Why no RAM upgrades for Dono-02/Dono-04 (Game Servers) servers?
Max RAM was raised from 4GB to 6GB; further increases are not available due to limited resources.

Update as of 2026, this is also due to the constrained supply chain in regards to memory.
### What happens if you charge back via PayPal or your bank?
See [Chargeback Policy Here](/policies/chargeback).
### How do I appeal a ban or suspension?
See [Appeals Guide Here](/appealing-a-ban).

---

## Databases
### Postgres
Use `container` as the username. Connection string format:

```text
postgres://container:<PASSWORD>@<node>.danbot.host:<port>/postgres
```
### MongoDB
Connection string format:

```text
mongodb://admin:password@nX.danbot.host:port/?authSource=admin
```

Replace `X` with your node number (use `dono-0X` for donator nodes). The password is in the Startup tab; use your server's port.
### Redis
Connection string format:

```text
redis://default:<PASSWORD>@dono-XX.danbot.host:<port>
```

Replace `dono-XX.danbot.host` with your server's node. The password is in the Startup tab under `Redis Password`; use your server's port from the main page.

--- 

## Node Status Meanings
### Wings offline
Panel access unavailable for your server.
### System offline
Node is offline; panel access and workloads are down.
### Maintenance
Node in maintenance; bot offline and panel access unavailable until it returns.
### Online
Node healthy and ready to use.

---

!!!info Last Updated:
September 21, 2026.
!!!
