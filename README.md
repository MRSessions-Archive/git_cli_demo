# Work in Progress (To be Posted on <https://blog.mrsessions.com>)
I will be using this repository to make changes on and demonstrate the different commands with terminal screenshots.

# Common Git Commands You Should Know Working on a Team 

Over the past few years of development, I've used Team Foundation Version Control (TFVC) and Git. Both are great repository tools (my opinion Git is a winner), and ones I have always used a GUI interface for, until recently. Even if you have used GUI tools to assist you in your daily Git adventures, you should still have an understanding of the Git CLI.

I use an Azure DevOps Git repository for both the company and startup I work for, and I use GitKraken, and it requires a pro subscription to use with Azure DevOps. In the startup, I have had a few developers come and go, and with some of them, they tend to use the Git CLI, and also have questions about how to do specific tasks like a Git rebase, because they might not understand some Git commands. At first, this was hard for me, because I was always comfortable working in GitKraken and other GUI tools.

So, recently, I decided that I was going to learn how to use the Git CLI so that I can best help my developers when they needed help. With this, I have decided that I would include a list of common git commands you should know when you are working in a team. That means that I won't cover how to initialize a repository or other tasks, but rather, common Git commands you can use. As a bonus, I have started using the Git CLI more than GitKraken now.

The list of commands I use, in no particular order:
git clone <repository url>
git checkout <branch>
git checkout -b <new-branch-name>
git fetch
git branch
git status
git log
git branch -r
git pull
git add .
git add <file>
git commit -m "<commit message>"
git push
git push --force
git branch -d <branch>
git branch -D <branch>
git rebase -i <>
git rebase <branch>
git rebase --abort
git rebase --continue
git stash
git stash pop
git stash apply
  
## Git Clone \<Repository Url\>
When you first join a team that uses Git, cloning the repository is generally the first thing you will need to do. Find a directory you want to use for storing your repository, on Mac and Windows I store my repositories in <documents/source/repos>. In your terminal type `git clone https://github.com/MRSessions/git_cli_demo.git`. Of course, use the correct clone URL here. Once that's cloned, you should be in the master/main branch.

## Git Checkout \<Branch\>
Within a Git repository, there are other branches that you will need to switch to, whether it's going to a develop or main branch, or back to your branch. Git checkout is specific to your local branches and the remote branches (since your last fetch). To move to another branch you would type `git checkout feature-branch`.

## Git Checkout -b \<New-Branch-Name\>
Git Checkout with a -b flag is similar to Git checkout, but you use this when you want to create a new branch off a branch you are currently in and immediately switch to it.

## Git Fetch
a `git fetch` is saying that you want to return the information from the remote repository and updates your local. This does so without manipulating your branch history on your local.

## Git Branch
`git branch` will show the branches that are on your machine.

## Git Branch -r
`git branch -r` will show the branches that are on the remote repository.

## Git Status
`git status` shows the status of the branch you are working in. If you have made changes to your files, but not committed yet, you will see the files you changed in a list.

## Git Log
`git log` allows you to be able to see information on the commits of the branch you are on. In this mode, you can press the 'space bar' or 'return' key to be able to scroll down. Press 'q' to exit. You can also combine this with other commands like `--oneline`.
## Git Pull
`git pull` allows you to get the latest commits from the tracked remote branch you are currently in.
## Git Add .
When you are working with files on your local branch, and you are ready to do a commit, you will need to make sure that your files are staged first. To do this, you would run `git add .`, this stages all of your files to be ready for commit.
## Git Add \<File\>
If you are working with multiple files, but only want to commit a few of those files, `git add <filename>` allows you to stage only that file. You can do this for all the files you want to add. After you commit, any files that you didn't stage will not be committed.

## Git Commit -m "\<Commit Message\>"
Git commit means that you are ready to create a commit to your branch with the staged changes that you have with a message (description) of that commit `git commit -m "my commit message"`

## Git Push

## Git Push --force

## Git Branch -d \<branch\>

## Git Branch -D \<branch\>

## Git Rebase \<branch\>

## Git Rebase -i \<Different Options\>
A git rebase interactive can be quite difficult at first, but once you understand the process, it gets better. One of the main reasons I use it is to squash commits on my branch together before I do any pull requests, but there's more to it. I will post an article that will go more in-depth on Git Rebasing.

## Git Rebase --continue

## Git Rebase --abort

## Git Stash

## Git Stash Pop

## Git Stash Apply
