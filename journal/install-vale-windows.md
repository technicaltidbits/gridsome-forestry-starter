---
title: Install the Vale CLI (Windows)
date: 2020-05-12
author: Deanna 
---
To install Vale on your computer, you'll need to use a package manager. Package managers allow you to install and update packages and libraries. 

Windows users can install Vale using [**Chocolatey**][Chocolatey link]. If you've already installed Chocolatey, skip to [step two](#heading-step-two:-install-vale). Otherwise, continue reading the instructions below. 

---

## Step one: Install Chocolatey 

1. Follow [these](https://chocolatey.org/install) steps to install Chocolatey on your computer.

2. To verify that you installed Chocolatey, run the command `choco -?`. If the installation was successful, the command prints the help documentation to the terminal.

## Step two: Install Vale

1. From the terminal, run the command `choco install vale`. You'll see some output in the terminal as Chocolatey installs Vale on your computer.

2. To verify that you installed Vale, run the command `vale -v` in the terminal. If the installation was successful, the command reports the latest, stable version of Vale.

---

That's all you need to do to install the Vale CLI! Next, you'll learn how to configure and customize Vale for your documentation needs. 

[Chocolatey link]: https://package.chocolatey.org/




