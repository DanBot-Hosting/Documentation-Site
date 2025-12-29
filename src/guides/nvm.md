---
label: Installing NVM (Node Version Manager)
order: 100
icon: server
---

# How to Install NVM on AIO Eggs

Node Version Manager (NVM) is a POSIX-compliant bash script to manage multiple active node.js versions.

## Installation Steps

Follow these steps to install NVM on your AIO egg:

1. Download the NVM installation script:
   ```bash
   wget https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh
   ```

2. Create the `.bashrc` file:
   ```bash
   touch ~/.bashrc
   ```

3. Run the installation script:
   ```bash
   bash install.sh
   ```

4. Load the NVM configuration:
   ```bash
   source ~/.bashrc
   ```

5. Done! NVM is now installed and ready to use.

## References

- [How to Install Node.js on Ubuntu Debian](https://computingforgeeks.com/how-to-install-node-js-on-ubuntu-debian/)
- [nvm-sh/nvm GitHub Repository](https://github.com/nvm-sh/nvm/blob/master/README.md)

!!!info Last Updated:
December 24, 2025.
!!!