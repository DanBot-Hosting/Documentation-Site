---
icon: file
---

# Node.js

[Node.js](https://nodejs.org) is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser.

---

## Requirements

- Have an account created and linked to the panel. [Click here if you have not done so already](/getting-started).

---

## Creating a Server

To create a free server, go into `#⌛╏commands` and run `DBH!server create nodejs [optional server name]` to create a free server. Once you have done so, the bot should return the following output.

If you are creating a donator server, instead run `DBH!server create-donator nodejs [optional server name]` 

## Configuration

---

### 1. Creating package.json

---

If you are going to install dependencies onto the server, which you most likely will, we will show you 2 methods to create a package.json file. **(If you already have a package.json file, skip this step)**

### Manually creating the file

Log in to the [panel](https://panel.danbot.host/), go to your server, and then files. Once here, create a new file and put the following in it (replace the dependencies with the ones you are using)
```json
{
  "dependencies": {
    "dependency": "1.0.0",
    "another-one": "3.2.1"
  }
}
```
Then save the file with the file name `package.json`.

JSON formatting must be strictly followed! If you have issues installing any modules, consider validating your `package.json` file with a [JSON formatter](https://jsonformatter.curiousconcept.com/#).

### Creating the file via `npm init`

Please make sure you have installed [node and npm](https://nodejs.org) before doing this.

Open up a command prompt/terminal, use `cd` to navigate to your project folder, and then run `npm init`. Once complete, fill out the info it asks for, or just press enter to use the text in the brackets. Once this is complete, you should have a package.json file.

Now, log in to the [panel](https://panel.danbot.host/), go to your server, and then files. Once here, click on upload and upload your package.json file.

If you want to add your dependencies to the file if you haven't already, take a look at [manually creating a file](/server-types/nodejs/#manually-creating-the-file).

---

### 2. Uploading or creating your code files

---

If you plan to use a port for a website or API, please make sure to get the right port from your server console, looking for something like `dono-XX.danbot.host:PORT`.

### Create from scratch

If you don't have anything coded yet, and you want to code it by the way, go to the panel, your server, and then files. There you have three buttons: Create directory, Upload, and New File. Click New File. There you can code your app.

When you finish coding, name the file something like `index.js` and save it.

Once you do that, you're done and you can start your server.

### Uploading Code Files

If you already made something and you want to upload it, you need to compress the file into a .zip or .tar.gz file, and then upload it. **Make sure that you do not compress the `node_modules` file as it's automatically installed when the server starts.** When the file finishes uploading, click the 3 dots and click "unarchive". **Make sure your main file is in the root folder and named index.js unless you know how to use a custom file name.**

If you just have a single file (e.g., index.js), you can just upload that without compressing anything.