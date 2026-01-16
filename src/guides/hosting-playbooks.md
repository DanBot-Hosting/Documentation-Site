# Hosting Playbooks

## Node.js / JavaScript apps
1. Create a server with `DBH!server create aio`.
2. Upload files and add `start.sh`:
```bash
npm i && node .
bash
```
3. For TypeScript:
```bash
npm i && npm run compile
node dist/index.js
bash
```
4. In Startup, set the command to `bash start.sh`, then restart/start the server. Install packages via `dependencies` in `package.json`.

## Python apps
1. Create a server with `DBH!server create python` or `DBH!server create aio`.
2. Upload files and add `start.sh`:
```bash
pip install -r requirements.txt && python3 main.py
bash
```
3. In Startup, set the command to `bash start.sh`, then restart/start the server.

## Proxied domains not using HTTPS
- Enable Force HTTPS by unproxying/reproxying or switching Cloudflare from DNS-only to Proxied (orange cloud), then in SSL enable "Always HTTPS."


> **Last Updated:**  
> January 16, 2026.
