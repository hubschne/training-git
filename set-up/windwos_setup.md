# Setup for Windows (PowerShell, VS Code, Git & GitHub)

## Open PowerShell

PowerShell is a command-line application that allows us to install and configure software using text commands.
1. Press the **Windows key**
2. Search for **PowerShell**
3. Right-click **PowerShell**
4. Select **Run as administrator**

# Install Chocolatey, the Windows package manager

Chocolatey is a package manager for Windows. It allows us to install software directly from PowerShell.


Copy and paste the following command into PowerShell and press Enter:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Close PowerShell and open it again.

Verify the installation:

```powershell
choco --version
```

You should see a version number.

---

# Install VS Code

VS Code (Visual Studio Code) is the editor we will use to write and edit code.

Install it with:

```powershell
choco install vscode -y
```

Verify the installation:

```powershell
code --version
```

If the command is not recognized, close and reopen PowerShell and try again.

---

# Install Git

Git is a version control system that allows us to track changes in code and collaborate through GitHub.

Install Git:

```powershell
choco install git -y
```

Verify the installation:

```powershell
git --version
```

You should see a version number.

---

# Configure Git

Git uses your name and email address to identify who created commits.

Replace the example values with your own information:

```powershell
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Configure Git to only allow fast-forward pulls. This prevents Git from creating unexpected merge commits when pulling changes:

```powershell
git config --global pull.ff only
```

Configure Git to use `main` as the default branch name for new repositories:

```powershell
git config --global init.defaultBranch main
```


---

# Setup an SSH Connection to Your GitHub Account

SSH keys allow GitHub to securely recognize your computer. Once configured, you won't need to enter your GitHub credentials every time you interact with repositories.

## Generate an SSH Key

Run:

```powershell
cd ~
ssh-keygen -t ed25519
cat .ssh/id_ed25519.pub | clip
```

When asked where to save the key, simply press **Enter**.

When asked for a passphrase, you can either:

- Enter one for additional security
- My recommendation: Press **Enter** to skip



Your SSH key is now copied to your clipboard.

## Add the Key to GitHub

1. Open GitHub in your browser.
2. Click your profile picture.
3. Open **Settings**.
4. Open **SSH and GPG keys**.
5. Click **New SSH key**.
6. Give the key a name (for example: *Work Laptop*).
7. Paste the key from your clipboard.
8. Click **Add SSH key**.

---

# Verify the SSH Connection

Run:

```powershell
ssh -T git@github.com
```

The first time, GitHub may ask:

```text
Are you sure you want to continue connecting (yes/no)?
```

Type:

```text
yes
```

and press Enter.

If everything is configured correctly, you should see a message similar to:

```text
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

---

# Final Check

You should now have:

- PowerShell configured
- Chocolatey installed
- VS Code installed
- Git installed
- Git configured
- An SSH key connected to GitHub

