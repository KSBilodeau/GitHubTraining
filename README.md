# The Unofficial GitHub Training Repo

This repo is a dedicated location for teachers and students to work together through various simple git related tasks in order to learn the importance of source version control software like Git.  Simply follow the directions in order either as an individual or a group, and you should have no trouble learning everything you need for using git in basic projects.

## Table of Contents:

1. [Installation](#step-1-git-installation-and-environment-prep)
2. [Online Repo Host](#step-2-create-a-github-account)
3. [Alternative FOSS Repo Host](#step-2-alternative-create-an-ablehub-account)

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

## Step #2: Create a GitHub Account

GitHub - the website you are currently viewing this tutorial on -
is a source sharing website that allows you to upload your git repositories.
In order to start uploading your own repos, you will need to setup an account with the service.

##### First Step: Navigate to the GitHub website

You can find GitHub at [https://github.com/](https://github.com/) and it should look like this:

[![](https://gcdnb.pbrd.co/images/ePnF71gnnTBZ.png?o=1)](https://gcdnb.pbrd.co/images/ePnF71gnnTBZ.png?o=1)

##### Second Step: Register

Then click on the sign up button in the top right corner, as shown:

[![](https://gcdnb.pbrd.co/images/gWdkh3hQA5kL.png?o=1)](https://gcdnb.pbrd.co/images/gWdkh3hQA5kL.png?o=1)

##### Final Step: Follow Registration Instructions

You will then be taken to a page that should look like the following image:

[![](https://gcdnb.pbrd.co/images/6G93BMn2S7NC.png?o=1)](https://gcdnb.pbrd.co/images/6G93BMn2S7NC.png?o=1)

Follow the instructions from then on and you should have successfully created a GitHub account!

## Step 2 ALTERNATIVE: Create an AbleHub Account

If you would like a FOSS alternative for hosting your git repositories, then look no further than AbleHub - a lightweight completely open source alternative for hosting git repos.

##### First Step: Navigate to the AbleHub website

You can find the AbleHub website at [](), and it should like this:

[![](https://gcdnb.pbrd.co/images/sQUnHiuWVKdj.png?o=1)](https://gcdnb.pbrd.co/images/sQUnHiuWVKdj.png?o=1)

##### Second Step: Register

Then click on the register button in the top right corner, as shown:

[![](https://gcdnb.pbrd.co/images/QkSt2A2mXl1x.png?o=1)](https://gcdnb.pbrd.co/images/QkSt2A2mXl1x.png?o=1)

##### Final Step: Follow Registration Instructions

You will then be taken to a page that should look like the following image:

[![](https://gcdnb.pbrd.co/images/94ic71QqJJWD.png?o=1)](https://gcdnb.pbrd.co/images/94ic71QqJJWD.png?o=1)

Follow the instructions from then on and you should have successfully created a GitHub account!