# Auto push Logseq changes to remote repository

`content below writen in linux environment`

## Concept

- everytime logseq commits changes
- it should also push to remote repository
- to achieve auto sync


## prerequisite

- have git repository setup i.e GitHub

## Steps to setup auto push

1. add remote url on your logseq i.e GitHub

```shell
git add remote <git remote url.git>

```


2. locate logseq .git hooks directory 

- open your current logseq directory
- use text editor and open .git file
- something similar as below

```
gitdir: /Users/peter/.logseq/git/desktop_logSeq/.git
```

3. copy post-commit file to git hooks directory found in step 2

- sample directory

```
/Users/peter/.logseq/git/desktop_logSeq/.git/hooks
```

- directory after copy

```
applypatch-msg.sample
commit-msg.sample
fsmonitor-watchman.sample
post-commit                  <-- this file copied
post-update.sample
pre-applypatch.sample
pre-commit.sample
pre-merge-commit.sample
pre-push.sample
pre-rebase.sample
pre-receive.sample
prepare-commit-msg.sample
push-to-checkout.sample
update.sample
```

- update the file permission

```shell
chmod 744 post-commit
```


## Voilà, enjoy auto psuh
