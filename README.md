# The Unofficial GitHub Training Repo

This repo is a dedicated location for teachers and students to work together through various simple git related tasks in order to learn the importance of source version control software like Git.  Simply follow the directions in order either as an individual or a group, and you should have no trouble learning everything you need for using git in basic projects.

##Table of Contents:

1. [Installation](#step-1-git-installation-and-environment-prep)

## Step #1: Git Installation and Environment Prep

##### Windows:

Get the official binary from [here](https://git-for-windows.github.io/) and follow the installation instructions.

##### MacOS:

For MacOS, there are currently three main options available in terms of installation options.  Choose whichever is most compatible with you and or your school's application installation policy:

1. Direct Binary Installation - get the DMG file from the same website as that you can find under the windows installation section aka [here](https://git-for-windows.github.io/).

2. Homebrew - for those who already have the Homebrew package manager installed already, then you can simply type the following into your terminal application:
```bash
brew install git
```
For those who wish to use the Homebrew package manaeger but do not have it already installed, simply run the following command and restart your terminal:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
After that, you should be able to run the top command without any issue.
3. MacPorts - for those who already have the MacPorts package manager installed, you can simply type the following into your terminal (do note this will require inputting an root user password):
```bash
sudo port install git
```
For those who wish to use the MacPorts package manaeger but do not have it already installed, please consult the [MacPorts installation page](https://www.macports.org/install.php) for information regarding its installation.

##### Linux

There are several package managers available, so for the purposes of this tutorial, we shall provide the installation commands that are provided on the git main install page; however, if you do not use either of these package managers, please consult your documentation:
1. DNF for Fedora and other RPM based Systems
```bash
sudo dnf install git-all
```
2. Apt-Get for Debian Based Systems such as Ubuntu
```bash
sudo apt install git-all
```
3. Pacman for Arch Linux
```bash
pacman -S git
```

##### ALL PLATFORMS

Finally open your terminal and run the following commands:

```bash
git config --global user.name "REPLACE_WITH_USERNAME"
git config --global user.email "REPLACE_WITH_EMAIL"
```