# Git/Gihub Sample Questions:

## Explain version control:

Version control (VCS) is a way to keep track of changes made to a project's file over time. It is commonly used by software developers when working on a group project. Some of the purposes of VCS includes: tracking changes, collaboration, branching and merging, documentation, backup. Here are examples of some version control systems: git, mecurial, subversion, gitlab, and bitbucket.

## Explain difference between git and github

Git and Github may look alike but they are distinct.

Git

Git is a version control system that was developed by Linus Torvalds, a Finnish-American software engineer. It allows multiple developers to work on the same project simultaneously. Git enables users to track changes, revert to changes, and work on different branches at the same time. Git provides commands like `git init`, `git clone`,  `git add`,  `git commit`, `git status`,  `git log`, `git reset`, `git revert` to mange changes. Git is the VCS itself.

GitHub

GitHub, on the other hand, is a web-based platform that provides hosting for Git repositories. It adds a user interface and a set of features on top of Git. GitHub makes collaboration easier by providing tools for code review, issue tracking, project management, and more. 

## List 3 other github alternatives

- GitLab
- Bitbucket
- SourceForge

## Explain the difference between git fetch and git pull

`git fetch`:

git fetch retrieves any new changes (commits, branches, tags, etc.) from the remote repository without modifying your working directory or merging the changes into your local branches.

After fetching, you can inspect the changes and decide when and how to integrate them into your local branches

`git pull`:

Pull, on the other hand, is a combination of two actions: git fetch followed by git merge.

It fetches the changes from the remote repository and automatically merges them into your current branch.

This means that git pull not only updates your remote-tracking branches but also modifies your working directory and local branches.

## Explain in simple terms git rebase and the command for it

`git rebase` is a Git command used to integrate changes from one branch into another by moving or combining a sequence of commits to a new base commit. it can be useful for maintaining a clean and linear commit history.

Imagine you have a branch (let's call it `develop`) where you've made some commits, but in the meantime, the `main` branch has also progressed with new commits. If you want to add the changes from `main` into your `develop` branch, you could use `git rebase`.

The basic syntax for `git rebase` is:

```bash
git rebase <base-branch>
```

For example, if you are on the `develop` branch and want to rebase it onto the latest commits from `main`, you would do:

```bash
git checkout develop
git rebase main
```

## Explain in simple terms git cherry-pick and the command for it 

`git cherry-pick` is a command in Git that allows you to copy a specific commit from one branch and apply it onto another branch.

`commit-hash` helps you identigy the commit you want to pick (apply) onto the current branch.
Here's a step-by-step breakdown:

1. Identify the commit you want to copy by looking at the commit history. You'll see a unique hash associated with each commit.

2. Switch to the branch where you want to apply the commit.

3. Run the `git cherry-pick` command with the commit hash you want to pick.