# Fixing `EnvironmentError - No space left on device`

This increases your container's TEMP storage; it does **not** add more disk space.

## Prerequisites
- PYTHON server

## Steps
1. On the PYTHON server, create a directory at `home/container/TEMP`.
2. If the issue happens while installing `requirements.txt`, run:
```text
pip3 install --cache-dir="$HOME/TEMP/" -r requirements.txt
```
3. If the issue happens while running code, export the TEMP directory:
```text
export TMPDIR=$HOME/TEMP
```
   - Note: the TMPDIR export is wiped on reboot.

## Making TMPDIR permanent
1. Create `run.sh` with:
```text
export TMPDIR=$HOME/TEMP
# replace this comment (this line) with your current Startup Command
```
2. Set the Startup Command (Startup category) to `bash run.sh`.

> Tip: Splitting up your `requirements.txt` can help if PIP installs are failing with this error.  
> Tip: Ensure `run.sh` is located where it can reach any file referenced by the Startup Command in this script.


> **Last Updated:**  
> January 16, 2026.
