# How to Install Oh My Bash (OMB) for Bash Shell

Oh My Bash (OMB) is a community-driven framework for managing your Bash configuration. It comes with a variety of plugins and themes to enhance your Bash experience. Here's how you can install Oh My Bash on your system:

## Step 1: Update Your System

Before installing Oh My Bash, make sure your system's package index is up to date:

```bash
sudo apt-get update
```

## Step 2: Install Git
Oh My Bash requires Git to download and install. If you don't have Git installed, you can install it using:

```bash
sudo apt-get install git
```

## Step 3: Install Oh My Bash

To install Oh My Bash, run the following command in your terminal:

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```
This script will clone the Oh My Bash repository to your home directory, install it, and set up your Bash configuration.

## Step 4: Configure Oh My Bash

After installation, you can start configuring Oh My Bash:
1.Changing Themes
	- Oh My Bash comes with several themes. To change the theme, edit the ~/.bashrc file:
	- Open the ~/.bashrc file in your preferred text editor:

```bash
nano ~/.bashrc
```

Find the line that says OSH_THEME="font". Change "font" to your desired theme. For example, to use the agnoster theme, modify the line to:

```bash
OSH_THEME="agnoster"
```

Save the file and exit the text editor (for nano, press Ctrl + X, then Y, then Enter).

Apply the changes:

```bash
source ~/.bashrc
```

## Adding Plugins
Oh My Bash also supports various plugins to extend its functionality. To enable plugins:

- Open the ~/.bashrc file:

```bash
nano ~/.bashrc
```
Find the line that says plugins=(). Add your desired plugins inside the parentheses, separated by spaces. For example, to enable the git plugin, modify the line to:

```bash
plugins=(git)
```
Save the file and exit the text editor.

Apply the changes:

```bash
source ~/.bashrc
```

## Step 5: Updating Oh My Bash
To keep Oh My Bash up to date, use the built-in update command:

```bash
upgrade_oh_my_bash
```

Uninstalling Oh My Bash
If you decide to uninstall Oh My Bash, you can do so with the following command:

```bash
uninstall_oh_my_bash
```
This will revert your Bash configuration to its state before installing Oh My Bash.

By following these steps, you can enhance your Bash shell with themes and plugins using Oh My Bash.