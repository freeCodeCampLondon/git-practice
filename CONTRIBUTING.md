# Contributor's Guide

The process consists of 6 main steps:

1 - Forking: Making a copy of the project on your github.
2 - Cloning: Making a local copy of the project.
3 - Branching: Creating another version to work in before using master.
4 - Rebasing: Making sure your branch is up to date with the main project.
5 - Push: Adding your changes to your github
6 - Pull: Requesting for your changes to be added to main project.


## Forking and Cloning Locally

1.  Go to the main page for the repository: <https://github.com/FreeCodeCampLondon/git-practice>
2.  Click on the 'Fork' button in the upper right hand corner. [Detailed instructions here](https://help.github.com/articles/fork-a-repo).
3.  Once this is done you will be taken to your copy of the repository at `yourUserName/github-practice`
4.	Clone your fork locally and `cd` into the new directory:

    `git clone https://github.com/yourUserName/github-practice.git`

    `cd FCCLND`

4.  Add the main repository as a remote branch so that you can rebase later

    `git remote add upstream https://github.com/FreeCodeCampLondon/FCCLND.git`

## Creating Branch

1. Create new branch to make changes on and move to that branch

    `git checkout -b update/your-name`

## Make Changes

1. Open text document campers.txt and add your name to the list.

## Rebasing from Upstream

Before making your Pull Request you need to make sure that you are up to date with the main repository.

1.	Switch to the `master` branch

    `git checkout master`

2.	Update `master` to be inline with the main repository

    `git pull --rebase upstream master`

3.  (Optional) Push `master` to your fork for good measure.

    `git push origin master --force`

4.  Switch back to your branch (change `type/branch-name` to your branch name)

    `git checkout update/your-name`

5.  Rebase your branch from master

    `git rebase master`

6.  Push your branch to your fork

    `git push origin update/your-name`

7.  You are now ready to submit a Pull Request


## Submitting a Pull Request

1.  Once you have pushed all your changes to your fork navigate to the GitHub page for your fork.
2.  In the Branch menu, choose the branch that you were working on.
3.  On the right of the page click on **New Pull Request**
4.  Change the title to short description of the issue you have worked on
5.  In the Comment section write a brief outline of the changes you have made.
6.  End the comment with a new line with the text 'Closes' followed by a '#' and the issue number that your Pull Request relates to. e.g. `Closes #4`
7.  Click on **Create pull request**
8.  Your Pull Request will be reviewed by the core team before being merged into the main repository.
  
