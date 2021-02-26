### User-specific configuration
```bash
git config --global user.username jdoe
git config --global user.name "John Doe"
git config --global user.email john.doe@domain.org
```

### Aliases
```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm commit
git config --global alias.dt difftool
git config --global alias.mt mergetool
```

### Diff & Merge using `meld`
```bash
git config --global diff.tool meld
git config --global difftool.meld.cmd "meld \"\$LOCAL\" \"\$REMOTE\""
git config --global difftool.prompt false

git config --global merge.tool meld
git config --global mergetool.meld.cmd "meld \"\$LOCAL\" \"\$BASE\" \"\$REMOTE\" --output \"\$MERGED\""
git config --global mergetool.keepBackup false
```
