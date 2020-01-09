# Git Bisect

## Using regex to find a missing text in a file

You only need to pass the path to the folder if you get an arguments to large exception

    git grep <regex pattern> $(git rev-list --all -- <path to file or folder>) -- <path to file or folder>
 
lets look at the commit dates
    
    git show -s --format=%ci <commit hash A>
    git show -s --format=%ci <commit hash b>
 

git bisect takes a bad and good commit

    git bisect start HEAD <good commit hash> --
    
I am using ripgreap (its better). it returns the 0 and 1 exit codes required by bisect

    git bisect run sh -c 'rg '<regex pattern>' <path to file>'