# Rebase

## Introduciton

![image](before-rebase.jpg)
- Branch `main` has commits `a`, `c`, `d`, …. in it (`a` is latest)
- Branch `feature-sds` has commits `b`, `c`, `d`,… in it (`b` is latest)
- `feature-sds` was branched out of main when commit “a” was not made.
- After commit `a` is made, “feature-sds” is not based on the latest main

## Problem
- When feature-sds branch is tested, it doesn’t contain commit `a`, so there are chances the test behaves gives different result in main branch after merge
- There may be merge conflicts while merging 

## Result of Rebase
![image](after-rebase.png)
- Branch `main` has commits `a`, `c`, `d`, …. in it (`a` is latest)
- Branch `feature-sds` has commits `b`, `a`, `c`, `d`,… in it (`b` is latest)

## Benefits of Rebase
- Testing the feature branch is more reliable
- The probability of the merge conflict is not there after rebase is not there

## What is rebase
- Changing the base commit of the a branch is rebasing

## Points to note
- When rebased, force push is needed
- Rebase only feature branches that are maintained by one dev, do not rebase main/develop branch

## How to rebase

### Command Prompt
- Clone the repo by the command `git clone https://github.com/GetGitReady/learn-rebase.git`
- Go to the repository by the command `cd learn-rebase`
- Check out the feature branch by the command `git checkout`
- Ensure you feature branch is checked out by the command `git branch`
- Run the command `git rebase main`

### Source Tree
- Clone the repo by the command `git clone https://github.com/GetGitReady/learn-rebase.git`
- Open the folder in Source Tree
![image](source-tree-open.png)
- Ensure remote branches are shown
![image](source-tree-show-remote-branches.png)
- Check out the branch `feature-sds`
![image](source-tree-checkout-branch.png)
- Ensure branch `feature-sds` is checkout out
![image](source-tree-ensure-branch-checked-out.png)
- Right click on `main` branch label and choose `Rebase` option
![image](source-tree-rebase.png)

### Visual Studio
- Clone the repo by the command `git clone https://github.com/GetGitReady/learn-rebase.git`
- Open the folder in visual studio
![image](open-visual-studio.png)
- Check out branch `feature-sds`
![image](checkout-branch-visual-studio.gif)
- Rebase on to the main
![image](rebase-visual-studio.gif)

