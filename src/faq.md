# DBH FAQ & Guides

## Donations & Premium Servers
- **How do I get donator servers? How do I donate? How do I get better servers?**
  - Donate at https://paypal.me/DanBotHosting (minimum $1, priced at `$0.50` per premium server).
  - Include your Discord ID in the notes. Open a ticket and provide a screenshot plus the transaction ID so staff can process it.
- **What is the price of DBH VPN?**
  - Free, with paid add-ons such as static IPs and premium locations (currently in beta).

## Common Issues
- **"No Space" error even with free disk**
  - Known issue from RAID setup on the new SSDs; being worked on.
- **Out-of-space errors when installing packages**
  - Installs use a temp directory limited to 100MB on the host. Packages larger than that limit fail with out-of-space messages.
  - For the container TMPDIR workaround, see: [Fixing `EnvironmentError - No space left on device`](fixing-no-space-temp.md).

## Hosting Support
- **Do you support Lavalink servers?**
  - Yes. Limit RAM to 2GB, or use the public instance: IP `63.141.232.244`, Port `1221`, Password `DBH`.
- **What eggs currently have issues?**
  - Broken eggs: N/A
  - Outdated eggs: N/A
- **Node IPs**
  - Provided on request; check the panel or ask staff if you need specifics.
- **What hosts do we use?**
  - Primarily Nocix and Hetzner, followed by Server.net and a few colocated VPS hosts.
- **Having issues with the DBH Pterodactyl API?**
  - Set the user agent to `DBH` when calling the API.
- **Proxied domains not using HTTPS**
  - Enable Force HTTPS by unproxying/reproxying or switching Cloudflare from DNS-only to Proxied (orange cloud), then in SSL enable "Always HTTPS."
  

## Policies
- **What are you not allowed to host?**
  - See the full list here: https://docs.danbot.host/policies/policy-list/
- **What is the difference between Free Nodes and Donator Nodes?**
  - Donator servers are paid and limited to donors or code claimers.
- **What's the catch? Why is it free?**
  - Started in 2016 to help friends test projects; it grew into a business and a learning platform for system administration. Using DBH helps it grow and supports ongoing learning.
- **Why don't we change startup commands for users?**
  - Avoids false anti-abuse flags and prevents unstable startup flags from harming servers or nodes.
- **Why no additional allocations for servers?**
  - Allocations control server counts; extra allocations would skew usage data.
- **Why no RAM upgrades for Dono-02/Dono-04 servers?**
  - Max RAM was raised from 4GB to 6GB; further increases are not available due to limited resources.
- **What happens if you charge back via PayPal or your bank?**
  - Immediate ban. Per ToS you may request a no-questions-asked refund within 14 days; after that, open a ticket for help.

## Databases
- **Postgres**
  - Use `container` as the username. Connection string format:
    - `postgres://container:<PASSWORD>@<node>.danbot.host:<port>/postgres`
- **MongoDB**
  - Connection string format:
    - `mongodb://admin:password@nX.danbot.host:port/?authSource=admin`
  - Replace `X` with your node number (use `dono-0X` for donator nodes). The password is in the Startup tab; use your server's port.

## Node Status Meanings
- Wings offline: Panel access unavailable for your server.
- System offline: Node is offline; panel access and workloads are down.
- Maintenance: Node in maintenance; bot offline and panel access unavailable until it returns.
- Online: Node healthy and ready to use.


> **Last Updated:**  
> January 16, 2026.
