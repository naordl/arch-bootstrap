# Arch Bootstrapper

## Introduction

This is a bootstrapping script intended to deploy a fully configured and personalized Arch Linux user environment from scratch.

It installs my favorite Linux programs and pulls down my [configuration files repository](https://github.com/naordl/dotfiles).

## Screenshots

![](/img/gpu-drivers.png)
![](/img/laptop-specific.png)

## Step-By-Step Guide

### Prerequisites

Have a base install of Arch Linux ready, along with a user that has `sudo` privileges. You can achieve this by editing the `/etc/sudoers` file using the following command:

```
$ EDITOR=vim visudo
```

You may change the `EDITOR` variable to your favorite text editor.

Uncomment the line starting with `%wheel` and save the file.

After this, clone this repository into your `$HOME/.local/src` directory, in order to keep the `$HOME` directory clean. This is a reocurring theme in my configuration files.

```
$ mkdir -p ~/.local/src
$ cd ~/.local/src
$ git clone https://github.com/naordl/arch-bootstrap.git
```

This is also the same directory where the bootstrapping script will download my [configuration files repository](https://github.com/naordl/dotfiles) by default.

If you woud like to do things your own way, you may alter the `arch-bootstrap.sh` script according to your preferences.

### Running the script

First, make sure the script is executable by running the following command:

```
$ cd arch-bootstrap
$ chmod +x arch-bootstrap.sh
```

Then, you can execute it:

```
$ ./arch-bootstrap.sh
```

A dialogue box should appear which will guide you through the installation process.

If your installation was completed successfully, you should see the following message in the console:

```
Successfully finished installing packages, deploying dotfiles, and configuring the system.
Reboot with the command 'reboot' for the changes to take effect.
```

Enjoy!
