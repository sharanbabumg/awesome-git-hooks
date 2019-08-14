<h1 align="center">
  <a href="https://git-scm.com/">
  <img width="455" src="https://github.com/compscilauren/awesome-git-hooks/blob/master/git-logo.png" alt="Awesome Git Hooks"></a><br>Awesome Git Hooks
</h1>

<p align="center"><a href="https://awesome.re"><img src="https://awesome.re/badge-flat2.svg" alt="Awesome Lists"></a></p>

# Awesome Git Hooks

> :anchor: Easy-to-use git hooks for automating tasks during git workflows.

Git hooks are custom scripts you can use to automate tasks which are triggered before or after a git command is executed. There are two groups of these hooks: client-side and server-side. Client-side hooks are triggered by operations such as committing and merging, while server-side hooks run on network operations such as receiving pushed commits. This repo contains helpful resources as well as a variety of git hook scripts that can be easily customized to serve different purposes.

:heavy_check_mark: Nothing to install/download

:heavy_check_mark: Code is well-documented

:heavy_check_mark: Grab & go! Copy the code you want to use and paste into your .git/hooks folder

## Contents

- [Git Hook Scripts](#git-hook-scripts)
  - [commit-msg](#commit-msg)
  - [post-checkout](#post-checkout)
  - [post-update](#post-update)
  - [pre-commit](#pre-commit)
  - [prepare-commit-msg](#prepare-commit-msg)
  - [pre-push](#pre-push)
  - [pre-rebase](#pre-rebase)
  - [query-watchman](#query-watchman)
  - [update](#update)
- [Quick Start](#quick-start)
- [Tools](#tools)
- [Written Guides](#written-guides)
- [Video Guides](#video-guides)

## Git Hook Scripts

### commit-msg

- [enforce-insert-issue-number](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/commit-msg-hooks/enforce-insert-issue-number.hook) - Make sure user did not delete the ISSUE-\[#] string that was generated by prepare-commit-msg/insert-issue-number.hook.

### post-checkout

- [delete-pyc-files](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/post-checkout-hooks/delete-pyc-files.hook) - Delete all .pyc files every time a new branch is checked out.
- [new-branch-alert](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/post-checkout-hooks/new-branch-alert.hook) - Display a message when a new branch is checked out for the first time.

### post-update

- [update-server-info](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/post-update-hooks/update-server-info.hook) - Prepare a packed repository for use over dumb transports (e.g. http).

### pre-commit

- [format-code](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/pre-commit-hooks/format-code.hook) - Run command to format code and re-add any files modified after formatting.
- [search-term](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/pre-commit-hooks/search-term.hook) - Fail commit if a specific term is found in the code.
- [spell-check-md-files](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/pre-commit-hooks/spell-check-md-files.hook) - Check files with .md extension for spelling errors.
- [verify-name-and-email](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/pre-commit-hooks/verify-name-and-email.hook) - Fail commit if user.name or user.email is incorrect.

### prepare-commit-msg

- [include-git-diff-name-status](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/prepare-commit-msg-hooks/include-git-diff-name-status.hook) - Include the output of "git diff --name-status -r" into the message, just before the "git status" output.
- [insert-issue-number](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/prepare-commit-msg-hooks/insert-issue-number.hook) - Insert issue number to beginning of the commit message.

### pre-push

- [prevent-bad-push](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/pre-push-hooks/prevent-bad-push.hook) - Prevent push of commits where the log message starts with "WIP" (work in progress).

### pre-rebase

- [prevent-rebase](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/pre-rebase-hooks/prevent-rebase.hook) - Prevent topic branches that are already merged to 'next' branch from getting rebased, because allowing it would result in rebasing already published history.

### query-watchman

- [fsmonitor-watchman](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/query-watchman-hooks/fsmonitor-watchman.hook) - Output to stdout all files that have been modified since a given time.

### update

- [update](https://github.com/CompSciLauren/awesome-git-hooks/blob/master/update-hooks/prevent-unannotated-tags.hook) - Block unannotated tags from entering.

## Quick Start

1. Pick a hook, any hook! Try the "verify-name-and-email" one if you're not sure where to start.
2. Navigate to your project's hooks folder (.git/hooks).
3. You should see a list of files already in there. Create a new file called the exact commit type that you want to use (eg: "commit-msg", "pre-rebase", "pre-commit", etc). Do not give it an extension.

![create new file](create-new-file.gif)

4. Open your new file and paste the code from the hook you chose out of this repo (eg: [verify-name-and-email.hook](https://github.com/CompSciLauren/git-hooks/blob/master/pre-commit-hooks/verify-name-and-email.hook)).
5. Save file. Done! Now the git hook will be triggered automatically.

## Tools

- [Husky](https://github.com/typicode/husky) - Manage git hooks with a nice user interface.

- [Overcommit](https://github.com/sds/overcommit) - A fully configurable and extendable git hook manager.

- [Git Hooks](https://github.com/icefox/git-hooks) - Manage project, user, and global git hooks more easily.

## Written Guides

- [Git hooks documentation at git-scm.com](https://git-scm.com/docs/githooks)

- [Git Pro book by Scott Chacon and Ben Straub](https://git-scm.com/book/en/v2)

- [An Introduction to Git Hooks](https://www.sitepoint.com/introduction-git-hooks/)

- [Atlassian Tutorial on Git Hooks](https://www.atlassian.com/ru/git/tutorials/git-hooks)

- [Easy git hooks with husky](https://www.vojtechruzicka.com/githooks-husky/)

- [Git Hooked](https://www.javascriptjanuary.com/blog/git-hooked 'Git Hooked')

- [How To Use Git Hooks To Automate Development and Deployment Tasks](https://www.digitalocean.com/community/tutorials/how-to-use-git-hooks-to-automate-development-and-deployment-tasks)

- [Automate Your Workflow with Git Hooks](https://hackernoon.com/automate-your-workflow-with-git-hooks-fef5d9b2a58c)

- [Using JavaScript in Your Git Hooks](https://medium.com/@Sergeon/using-javascript-in-your-git-hooks-f0ce09477334 'Using JavaScript in Your Git Hooks')

- [An In-Depth Look at Git Hooks](https://dzone.com/articles/an-in-depth-look-at-git-hooks)

- [Git hooks and practical uses. Yes, even on Windows.](https://www.tygertec.com/git-hooks-practical-uses-windows/)

## Video Guides

- [Git Hooks Part 1 - Getting Started](https://www.youtube.com/watch?v=aB3eq52sZSU)

- [Git hooks and practical uses. Yes, even on Windows.](http://www.youtube.com/watch?feature=player_embedded&v=fMYv6-SZsSo&t=240s)

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)<br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
