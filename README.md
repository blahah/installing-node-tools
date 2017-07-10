# installing-node-tools

Cross-platform node tool installation instructions to be linked from READMEs/documentation

## Contents

- [Introduction](#introduction)
- [macOS](#macos)
- [linux](#linux)
- [windows](#windows)

## Introduction

You're here because you need to install a tool that uses nodeJS, and it's not obvious how to do that. These instructions try to make it as painless as possible.

Here are some things to be aware of:

- **don't** use the instructions on the NodeJS website
- **don't** use whatever package manager you use for your OS generally (e.g.`apt`, `brew`, `chocco`)
- **don't** use admin privileges or `sudo` when installing node or any node tool
- **do** use a nodeJS version manager - this lets you keep node up to date, and switch versions easily
- **do** install everything in userspace - this prevents complex permissions issues and limits security concerns

### Node.js version manager

Whatever operating system you use, you'll need to install Node.js. We recommend doing this using [**nvm**](https://github.com/creationix/nvm#installation) - the **n**ode **v**ersion **m**anager (or for windows, [`nvm-windows`](https://github.com/coreybutler/nvm-windows).

## macOS

### prerequisites: developer tools

If you're on macOS/OSX, you'll need to install either:

- XCode, Apple's developer environent, free from the mac App Store
- [the command-line developer tools](http://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/).

### installing `nvm`

Open a terminal and run this command:

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.30.1/install.sh | bash
```

If it fails because you don't have `curl` installed, try using `wget` instead:

```bash
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.30.1/install.sh | bash
```

Follow the instructions that appear in the terminal - it will ask you to close the terminal once it's done.

### installing `node`

After you've closed and re-opened your terminal, you'll need to tell `nvm` to install the latest version of Node, and set it as default:

```bash
nvm install 7
nvm use 7
nvm alias default 7
```

### installing a `node` tool:

```bash
npm install --global some-node-tool
```

## linux

### installing `nvm`

Open a terminal and run this command:

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.30.1/install.sh | bash
```

If it fails because you don't have `curl` installed, try using `wget` instead:

```bash
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.30.1/install.sh | bash
```

Follow the instructions that appear in the terminal - it will ask you to close the terminal once it's done.

### installing `node`

After you've closed and re-opened your terminal, you'll need to tell `nvm` to install the latest version of Node, and set it as default:

```bash
nvm install 7
nvm use 7
nvm alias default 7
```

### installing a `node` tool:

```bash
npm install --global some-node-tool
```

## windows

### installing `nvm-windows`

Go to the [downloads page](https://github.com/coreybutler/nvm-windows/releases) and download `nvm-setup.zip` for the latest version.

Unzip the downloaded file and run the included installer.

### installing `node`

Open your command-line program (we recommend [`cmder`](http://cmder.net/) if you don't have one yet), then run:

```
nvm install 7
nvm use 7
```

### installing a `node` tool:

```bash
npm install --global some-node-tool
```
