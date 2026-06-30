
## Typical git workflow


### Downloading a Project for the First Time

Creating a local copy (on your computer) of a project on github:

```bash
git clone <repository-url>
```


> You need to do this only once! 

 If you want to start working on it, change directions into the folder:

```bash
cd <repository-name>
```

And start editing in vs code:

```bash
code .
```

### Normal Daily Workflow (Making Changes)


Move into your repository:

```bash
cd <repository-name>
```

Check the status of your project

```bash
git status
```

> You can see the status of your file changes, in which branch you currently are

Download and apply the latest changes

```bash
git pull
```

If you are not there yet, switch to the branch you want to work on

```bash
git switch <branch-name>
```

OR: if you want to create a new branch: 

```bash
git switch -c <branch-name>
```
> The flag -c stands for create. You will create a new branch and directly switch to it.


Edit your file(s).

Then check git status again, to see which files have changed.

```bash
git status
```

Select all the files that you want to add to your next commit (put them into the staging area):

```bash
git add <file-name>
```

You can check again, if all the files are staged as you wanted to with `git status`. Afterwards commit your changes with: 

```bash
git commit -m "Describe what you changed"
```

> A commit should contain one logical change, not multiple.

> A practical rule: Commit early, commit often, but only commit changes that make sense together.

If you are happy with your changes, then upload them to github: 

```bash
git push
```

> Check the message printed in the terminal: Often when your newly created branch doesn't exist yet on github. If that's the case, the correct command is printed in the terminal, you can just copy and paste it and run the correct command again.

If everything worked out, you can go on github, refresh the page, and see your changes online.

at the end of your work, it's common to go back to the main branch. You can do that with 
```bash
git switch main
```
## Pull request

A Pull Request (PR) is a request to merge your changes from one branch into another (usually into `main`). It allows others to review your work before it becomes part of the project.

If all your work on your branch is completed, and you have commit all changes and pushed them to github, you can start opening a pull request (PR).

1. Go to your repo and there to PR. 
1. Create a new PR by clicking on "New pull request". The "base" branch is normally the main branch, the "compare" branch, your branch you have worked on.

1. Click on "create PR" and describe what you have done in this PR:
    - Use a short, descriptive title
    - Use the description to briefly explain:
        - What changed?
        - Why was it changed?
        - Is there anything reviewers should pay attention to?
1. Add people as reviewers that should check your work.
1. When people have approved your changes, you can close the PR (and for keeping the project clean, you can delete the branch)

> Don't forget to download these changes to your local repo: `git switch main` and then `git pull`.

