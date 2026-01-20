---
name: Setting up GitHub Actions
icon: book
---

# Connect GitHub to DBH (GitHub Actions)

1. Create an AIO server: `DBH!server create aio server-name` (AIO has Python, Node.js, etc.).
2. In your GitHub repo: Settings > Actions > Runners > New self-hosted runner (Linux).
3. Start your DBH server and follow the runner setup instructions (you may need to retry to catch prompts since the console hides them). Skip running `./run.sh` for now.
4. In Actions, click "set up a workflow yourself" and paste:
```yaml
name: DBH
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
jobs:
  build:
    runs-on: self-hosted
    steps:
    - name: Git pull
      run: |
        cd
        git init
        git pull https://github.com/[your-organization-or-profile]/[your-repo].git
        npm i
```
5. Save, then run `./run.sh` via a child process to keep the runner active.


> **Last Updated:**  
> January 16, 2026.
