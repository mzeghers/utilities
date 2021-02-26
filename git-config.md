If not on a Bash-like terminal, you may have to review escape characters.

### User-specific configuration
```bash
git config --global user.username jdoe
git config --global user.name "John Doe"
git config --global user.email john.doe@domain.org
```

### Aliases
```bash
git config --global alias.s "status -s"
git config --global alias.st status
git config --global alias.aa "add -A"
git config --global alias.co checkout
git config --global alias.cob "checkout -b"
git config --global alias.br branch
git config --global alias.cm "commit -a"
git config --global alias.dt difftool
git config --global alias.mt mergetool
git config --global alias.last "log -1 HEAD"
git config --global alias.wipe \!"git add -A && git commit -qm 'WIPE SAVEPOINT' && git reset HEAD~1 --hard"
```

More [here](https://githubtraining.github.io/training-manual/#/app_aliases), [here](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases), [here](https://haacked.com/archive/2014/07/28/github-flow-aliases/), [here](https://haacked.com/archive/2015/06/29/git-migrate/) and [there](https://haacked.com/archive/2017/01/04/git-alias-open-url/).

### Diff & Merge using `meld`
```bash
git config --global diff.tool meld
git config --global difftool.meld.cmd "meld \"\$LOCAL\" \"\$REMOTE\""
git config --global difftool.prompt false

git config --global merge.tool meld
git config --global mergetool.meld.cmd "meld \"\$LOCAL\" \"\$BASE\" \"\$REMOTE\" --output \"\$MERGED\""
git config --global mergetool.keepBackup false
```
