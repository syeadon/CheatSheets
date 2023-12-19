
# Tracked files

## Discard Changes in a Specific File: 

If you want to discard changes in a specific file, you can use the following command:

    git checkout -- filename


## Discard Changes in All Modified Files: 

To discard changes in all modified files in the working directory, you can use the following command:

    git checkout -- .

The . specifies the current directory, and this command will discard changes in all modified files.

## Discard Uncommitted Changes and Switch Branch: 

If you want to switch branches and discard any uncommitted changes, you can use the following command:   

    git checkout -f branch_name

Replace branch_name with the name of the branch you want to switch to. The -f (or --force) option is used to discard changes.

# Untracked Files

Always be careful when using `git clean` as it permanently deletes untracked files, and there's no easy way to recover them.

If you have untracked files that you want to remove, you can use the git clean command. Be cautious with this command, as it permanently deletes untracked files.

    git clean -f

The -f (force) option is required to perform the clean operation.

If you want to remove both untracked files and directories, you can use the -d option:

    git clean -fd

If you want to remove untracked files from the working directory but keep them in the repository (i.e., you don't want them to be tracked), you can use the following command:

    git clean -fX

This will remove only the untracked files but not untracked directories. The -X option tells Git to remove only the files that are not listed in the .gitignore file.

---

Links 

- [undo](https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git/)
- [discard](https://bartwullems.blogspot.com/2023/11/gitdiscard-local-changes.html)