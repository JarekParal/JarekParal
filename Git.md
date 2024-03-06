# Git

## Tools

[Mergetool meld](http://meldmerge.org/) (Linux, Windows)

```
git mergetool
```

## Git commands

### `git log`

Show the detailed `git log` tree history for all branches 

```
git log --all --decorate --oneline --graph
```

### `git clean`

Remove all unstashed files with `git clean`.

To remove also all ignored files, use `git clean -x`.

Other options:
- `-n` - dry run
- `-d` - remove also empty directories

More info on [this](https://git-scm.com/book/id/v2/Git-Tools-Stashing-and-Cleaning#_git_clean) page.

## Own Git aliases/shortcuts

You can set your own [Git aliases/shortcuts](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases). There are a few examples of my shortcuts:
```shell
git config --global alias.last 'log -1 HEAD'
git config --global alias.unstage 'reset HEAD --'
git config --global alias.l log
git config --global alias.st status
git config --global alias.br branch
git config --global alias.ch checkout
git config --global alias.co commit
```

## Plugins

### VS Code

#### [Git Graph Visualizes Branches in VS Code for Free](https://ardalis.com/git-graph-visualizes-branches-in-vs-code-for-free)

## Learning

### [A Simple Git Workflow for Github Beginners and Everyone Else](https://towardsdatascience.com/a-simple-git-workflow-for-github-beginners-and-everyone-else-87e39b50ee08)

Summary of basic commands.

### [Learning Git Branching](https://learngitbranching.js.org/)

Interactive web tutorial for Git branching and necessary commands. Very good way to learn with `git`.

### [The life-changing magic of git rebase -i](https://opensource.com/article/20/4/git-rebase-i)

How to use interactive `rebase`.

### [[CZ] Git: fixup!](https://filip-prochazka.com/blog/git-fixup)

How to use interactive `rebase` and `fixup` in Czech language.

### [Git-it is a (Mac, Win, Linux) Desktop App for Learning Git and GitHub](https://github.com/jlord/git-it-electron/tree/master/resources/contents/en-US/challenges)

App as basic tutorial for Git and GitHub PR (pull-request).

### [Pro Git book](https://git-scm.com/book/en/v2)
### [[CZ] Pro Git book](https://git-scm.com/book/cs/v2)

Official Git book.

### [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
