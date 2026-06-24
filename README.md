# Git Training
First steps with git and github.

## What is git?

- Distributed Version Control System
- can be used fully locally / offline

## What is github?

- Collaborate effectively online based on git (also version controlled)
- platform for a lot of development projects
- often used for Open-source community and contribution

## Trying out git

### Downloading the repo

1. Please clone the repository with 

```bash
git clone <repo-ssh-url>
```

2. Move into the repo: 

```bash
cd <repo-name
```

### Making your first change

1. Create a new branch: 

```bash
git switch -c <branch-name>
```

A2. dd description to one header in the [markdown cheatsheet](markdown-cheatsheet.md) and save the changes.

3. Check the status of your repository with `git status`.

4. Stage the changes with `git add <filename>`. 
5. And commit your changes. Explain in the commit message what you have added. Here is an example:

```bash
git commit -m "added section on how to create headers in md"
```

6. Upload your changes to github:

```bash
git push
```

Don't forget to check the message in your terminal: Copy the correct command to upload your changes to github by creating a new branch, named exaclty as your local branch. Paste the command in your terminal and execute it.

### Create your first PR

1. Create a PR. Compare the main branch with your branch name.

2. Add a title and description to your PR.

3. Add a reviewer and wait until they have reviewed your changes.

4. If the person has approved your changes, merge the branches, and close the PR and delete your branch.

5. On your local computer, change to the main branch:
`git switch main`and pull the new changes: `git pull`.


