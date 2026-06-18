# Setup for macOS (terminal, vscode, git)

Open the `terminal`on your computer (spotlight search (command + space),search for `terminal.app`). 

The Terminal is an application that allows you to interact with your computer using text commands. We will use it to install and configure development tools.

## Install homebrew, the mac packaging system

Homebrew is the most common package manager for macOS. It allows us to install software from the command line.

Please copy and paste the following command in your terminal and press enter.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

The terminal will ask you to type your password (of your computer), please write it, press Enter, and for the other steps, you can simply press Enter for the process to continue.

Please enter the next command to configure your .zprofile to recognize homebrew 

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
```

and then: 

```bash
source ~/.zprofile
```

To verify that this step worked please enter following: 

```bash
brew --version
```

A version should appear.

## Install vs code

VS Code (Visual Studio Code) is the editor we will use to write and edit code / markdown.

Please enter following command in your terminal:

```bash
brew install --cask visual-studio-code
```

Open vs code:

Press `Cmd+Shift+P`, type "Shell Command: Install 'code' command in PATH" and click on it.

## Setup your terminal

All of the following commands are not necessary, but might make your work with the terminal easier (prettifying your terminal), so I recommend you doing them :) 

```bash
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Add some terminal add-ons for easier usage of the terminal.

```bash
brew install zsh-autosuggestions zsh-syntax-highlighting starship
echo 'source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh' >> ~/.zshrc
echo 'source /opt/homebrew/share/zsh-autosuggestions/zsh-autosuggestions.zsh' >> ~/.zshrc
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
```

Install a "nerd font" for your terminal:

```bash
brew install --cask font-jetbrains-mono-nerd-font
```

Go to the settings of the terminal, under profile --> text --> font, change the font of the default theme to  "JetBrainsMono NF".

## Setup git and ssh connection to your github account

Let's install our version control system `git`.

```bash
brew install git
```

You can verify if it worked with this comand:

```bash
git --version
```

Some helpful standard configurations for your git workflow:


* Define your user name globally (change to your name)
    
    ```bash
    git config --global user.name "dein Name"
    ```
    
* You can define your E-Mail-Address globally ((change to your name)):
    ```bash
    git config --global user.email "deine E-Mail"
    ```
    
Git uses this information to identify who created commits.

* Config pull standard:
    
    ```bash
    git config --global pull.ff only
    ```
    
* Change name for Standard-Branch-Name:

    ```bash
    git config --global init.defaultBranch main
    ```


SSH keys allow GitHub to securely recognize your computer. Once configured, you won't need to enter your GitHub credentials every time you interact with repositories. So let's set it up:

```bash
cd ~
ssh-keygen -t ed25519
cat ~/.ssh/id_ed25519.pub | pbcopy
```

Press Enter when asked where to save the key.

You can either set a passphrase or **leave it empty** by pressing Enter.

The ssh key is now copied to your buffer. Navigate to your Profile on Github:
- go to Settings and then to SSH and GPG keys.
- click New SSH key and paste the contents of your buffer inside.
- Click Add SSH key.

To check that it worked please go back to your terminal and enter:

```bash
ssh -T git@github.com
```

The response should look like:
`Hi username! You've successfully authenticated...``



### Summary

At the end you should have:

- Homebrew installed
- VS Code installed
- Git installed
- A GitHub SSH key configured
- A customized terminal (optional)