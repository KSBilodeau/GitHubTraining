# The Unofficial GitHub Training Repo

This repo is a dedicated location for teachers and students to work together through various simple git related tasks in order to learn the importance of source version control software like Git.  Simply follow the directions in order either as an individual or a group, and you should have no trouble learning everything you need for using git in basic projects.

## Table of Contents:

1. [Installation](#step-1-git-installation-and-environment-prep)
2. [Online Repo Host](#step-2-create-a-github-account)
   1. [Alternative FOSS Repo Host (AbleHub)](#step-2-alternative-create-an-ablehub-account)
3. [SSH Keys](#step-3-ssh-key-for-pushes)
4. [Switch Branches](#final-step-switch-branches)

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

## Step 3: SSH Key for Pushes

While it may seem extremely tedious and unneccessary, having a connected SSH key will make future pushes much simpler in this world of increased internet security awareness.

##### First Step: Generate the Key

Simply use the following command in your terminal:

```bash 
ssh-keygen -t ed25519 -C "your_email@example.com"
```

*For older systems, you may need to use the following command if the top one does not work:*

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

This will then trigger the following prompts (follow the instructions in [] here, *do not type the [words]*):

```bash
Generating public/private algorithm key pair.
> Enter a file in which to save the key (/Users/you/.ssh/id_algorithm): [Press enter here]
> Enter passphrase (empty for no passphrase): [Type a passphrase here]
> Enter same passphrase again: [Type passphrase again here]
```

Congratulations, you have successfully created an SSH key!

###### Adding to your SSH agent

On most platforms, simply use the following command to add your key to your SSH agent:

```bash
ssh-add ~/.ssh/id_ed25519
# or for legacy systems
ssh-add ~/.ssh/id_rsa
```

On MacOS it is recommended to add the SSH passphrase to your keychain, so you will want to use this command instead:

```bash
ssh-add -K ~/.ssh/id_ed25519
# or for legacy systems
ssh-add -K ~/.ssh/id_rsa
```

On MacOS Monterey, -K and -A were deprecated, so use the following command instead:
```bash
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
# or for legacy systems
ssh-add --apple-use-keychain ~/.ssh/id_rsa
```

##### Final Step: Adding your key to your repo provider

For the purposes of this tutorial, we will only be covering adding to our supported providers; however, feel free to file an issue on this repo for me to add other providers if you believe it should be here as well.

###### GitHub

You are going to want to first login and navigate to the settings page, like so:

[![Login Page](https://gcdnb.pbrd.co/images/JlT0zshTfYwo.png?o=1 "Login Page")](https://gcdnb.pbrd.co/images/JlT0zshTfYwo.png?o=1 "Login Page")

[![Navigate to Settings](https://gcdnb.pbrd.co/images/Ll33w1lENnfD.png?o=1)](https://gcdnb.pbrd.co/images/Ll33w1lENnfD.png?o=1)

Then you are going to go to the `SSH and GPG keys` pane and click the `New SSH Key` button:

[![Navigate to SSH and GPG keys](https://gcdnb.pbrd.co/images/Fdxbyjt7Y4vo.png?o=1)](https://gcdnb.pbrd.co/images/Fdxbyjt7Y4vo.png?o=1)

[![Click `New SSH key`](https://gcdnb.pbrd.co/images/v1ToikakVRbe.png?o=1 "Click `New SSH key`")](https://gcdnb.pbrd.co/images/v1ToikakVRbe.png?o=1 "Click `New SSH key`")

Finally, you are going to fill in your key information and then click `Add SSH key`:

[![](https://gcdnb.pbrd.co/images/BourIaqRNCue.png?o=1)](https://gcdnb.pbrd.co/images/BourIaqRNCue.png?o=1)

To test your connection run the following command and follow its instructions:

```bash
ssh -T git@github.com
```

Should your connection be successful, the final prompt should read as follows:

```
> Hi username! You've successfully authenticated, but GitHub does not
> provide shell access.
```

###### AbleHub

You are going to want to first login and navigate to the settings page, like so:

[![Login Page](https://gcdnb.pbrd.co/images/xqmC7MvhZkWx.png?o=1 "Login Page")](https://gcdnb.pbrd.co/images/xqmC7MvhZkWx.png?o=1 "Login Page")

[![Navigate to Settings](https://gcdnb.pbrd.co/images/3CNRruZMURru.png?o=1)](https://gcdnb.pbrd.co/images/3CNRruZMURru.png?o=1)

Then you are going to go to the `SSH and GPG keys` pane and click the `New SSH Key` button:

[![Navigate to SSH and GPG keys](https://gcdnb.pbrd.co/images/zxWZWt37sTbK.png?o=1)](https://gcdnb.pbrd.co/images/zxWZWt37sTbK.png?o=1)

[![Click `New SSH key`](https://gcdnb.pbrd.co/images/clNqvAIKJa3A.png?o=1 "Click `New SSH key`")](https://gcdnb.pbrd.co/images/clNqvAIKJa3A.png?o=1 "Click `New SSH key`")

Finally, you are going to fill in your key information and then click `Add SSH key`:

[![](https://gcdnb.pbrd.co/images/uK5yeHZTp5Yo.png?o=1)](https://gcdnb.pbrd.co/images/uK5yeHZTp5Yo.png?o=1)

To test your connection run the following command and follow its instructions:

```bash
ssh -T git.ablecorp.us
```

Should your connection be successful, the final prompt should read as follows:

```
> Hi username! You've successfully authenticated, but AbleHub does not
> provide shell access.
```

## Final Step: Switch Branches

Now to continue this tutorial, please switch to the branch that matches your programming language of choice.