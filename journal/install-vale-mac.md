---
title: Install the Vale CLI (Mac)
date: 2020-05-12
author: Deanna 
---
To install Vale on your computer, you'll need to use a package manager. Package managers allow you to install and update packages and libraries. 

The best package manager for macOS is [**Homebrew**][Homebrew link]. If you've already installed Homebrew, skip to [step two](#heading-step-two:-install-vale). Otherwise, continue reading the instructions below.

---

## Step one: Install Homebrew 

1. To install Homebrew, enter this command into the terminal (feel free to copy and paste): `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`

2. To verify that you installed Homebrew, run the command `brew help`. If the installation was successful, the command prints the help documentation to the terminal.

## Step two: Install Vale 

1. From the terminal, run the command `brew install vale`. You'll see some output in the terminal as Homebrew installs Vale.

2. Verify that the `vale` command is now available by running `vale -v` in the terminal. If the installation was successful, the command reports the latest, stable version of Vale.

---

That's all you need to do to install the Vale CLI on your Mac! Next, you'll learn how to configure and customize Vale for your documentation needs. 

[Homebrew link]: https://brew.sh/
