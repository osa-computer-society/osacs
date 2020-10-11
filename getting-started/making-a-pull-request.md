---
description: >-
  In celebration of Hacktoberfest, here's a quick page to help you get started
  with contributing to open source!
---

# Making a Pull Request

I know getting started with contributing to open source can seem intimidating, but it's an amazing process and not too hard once you get started.

1. Say there's a repository, for example, `osa-computer-society/processing-showcase`, that you want to make changes to.
2. Go to the repository's page on GitHub and click "Fork" in the top-right corner - This creates a copy of the repository which _you_ own, and which you can change however you want.
3. Click on the big green "Code" button on your fork.
   1. If you have the GitHub CLI installed, choose that, and copy and paste the code into your terminal.
   2. Otherwise:
      1. Choose either HTTPS or SSH \(whichever your local installation of Git is set up to use\), and copy that url.
      2. Paste it into `git clone YOUR_URL_HERE` in your terminal.
      3. This will download a local copy of the code to your machine, as well as all of the files Git uses to manage history, remote repository information, etc. A "remote" called `origin` will be created that points to the version of your fork on GitHub.
4. You almost _never_ want to make changes directly to the _main_ \(or "master"\) branch of your code. This helps prevent bugs happening in "production", or the version of your code visible to your users. Instead, you want to make a new "branch", i.e. a new version of your code.
   1. To do this, make sure you're inside your project's folder \(aka "directory"\). If you're following along with these steps, this means you should run `cd REPOSITORY_NAME` \(this should be the last part of the URL without the ".git" at the end\).
   2. Type `git checkout -b YOUR_BRANCH_NAME` into your terminal. This is shorthand for:
      1. `git branch YOUR_BRANCH_NAME`
      2. `git checkout YOUR_BRANCH_NAME`
   3. It creates a new branch and switches over to it.
5. Make changes to whatever files you need, move files and folders around, write code, etc.
6. Once your code is _stable_ \(i.e. doesn't have any major bugs\) and looks like exactly how you want to present it, you can save it as a "snapshot in time", i.e. a **commit**.
   1. To do this, go to your terminal and type:
      1. `git add FILENAME1 FILENAME2 FOLDER1` etc. You can type `git add .` to add all changes in your working directory.
      2. This "stages" your changes and lets git know which changes you actually want to save.
      3. You can see the status of your git repository by running `git status`.
   2. Type `git commit -m "COMMIT_MESSAGE_HERE"`. This saves your commit using the commit message you specified. Since you checked out your new branch earlier, this will commit your changes to your new branch.
7. Now you want to push your changes to _your fork_ on GitHub.
   1. To do this, type `git push origin YOUR_BRANCH_NAME` into your command line. This updates the version of your repository that's on GitHub.
   2. If you type in `git log --all`, you'll see in the logs that `origin/YOUR_BRANCH_NAME` now points to the commit with your most recent changes.
8. Now, all of the changes you want to make to the _main_ repository are stored in the branch `YOUR_BRANCH_NAME` on _your fork_. To update the _main_ repository with these changes, you'll want to make a pull request.
   1. Go to your fork on GitHub. It should say "`YOUR_BRANCH_NAME` had recent pushes \(some time ago\)." Click on the button "Compare & pull request".
   2. Make sure that the base repository and base branch are correct, i.e. `osa-computer-society/processing-showcase` and `main` respectively, and that the head repository and branch are correct, i.e. `YOUR_USERNAME/processing-showcase` and `YOUR_BRANCH_NAME`.
   3. Title your pull request and fill out whatever the maintainers have asked you to in the template.
   4. Go ahead and click "Create pull request"! This will create a pull request on the main repository, and the maintainers should take a look at it eventually.

If you made it this far, **CONGRATULATIONS!** You've just made a contribution to the open source community! Give yourself a pat on the back and we hope you look forwards to contributing to open source!

