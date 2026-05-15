# Hosting Playbooks

List of different startup guides that you can use for Pterodactyl Servers.

## Node.js / JavaScript Applications:
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

---

## Python Applications:
1. Create a server with `DBH!server create python` or `DBH!server create aio`.
2. Upload files and add `start.sh`:
```bash
pip install -r requirements.txt && python3 main.py
bash
```
3. In Startup, set the command to `bash start.sh`, then restart/start the server.

---

!!!info Last Updated:
January 31, 2026.
!!!
