# Git Setup

## Git global setup

    git config --global user.name "Prename Name"
    git config --global user.email "email@example.com"
	git config --global diff.tool bc
	git config --global difftool.bc.path "c:/Program Files/Beyond Compare 4/bcomp.exe"
	git config --global merge.tool bc
	git config --global mergetool.bc.path "c:/Program Files/Beyond Compare 4/bcomp.exe"

	git config --list

Just remove the `--global` flag for local setup.
 Create a new repository

    git clone https://user@github.com/user/repo.git
    cd repo
    touch README.md
    git add README.md
    git commit -m "add README"
    git push -u origin master

## Existing folder

    cd existing_folder
    git init
    git remote add origin https://user@github.com/user/repo.git
    git add .
    git commit
    git push -u origin master

## Existing Git repository

    cd existing_repo
    git remote add origin https://user@github.com/user/repo.git
    git push -u origin --all
    git push -u origin --tags

## Update remote location

```bash
git remote rm origin
git remote add origin <new-location>
git branch --set-upstream-to=origin/master master
```

---

## Remove password prompt

Caution: this will store the password unencrypted on the disk! Only use if it's safe on your machine!

    git config credential.helper store

---

## Sign/verify commits

Use `git commit -S` by default for all commits

    git config --global commit.gpgsign true

Set default key

    git config --global user.signingkey <key-id>

---

## Git aliases

An alias to seekdir aliases

	git config --global alias.alias "! git config --get-regexp ^alias\. | sed -e s/^alias\.// -e s/\ /\ =\ /"
	
Prettier git log

	git config --global alias.logline "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"