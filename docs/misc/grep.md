# Grep

## RipGrep

Search for the text foo/{any text}/bar

    rg 'foo/\{.*\}/bar'


## Git Grep

To search a commit for content (i.e., codenot the commit messages):

    git grep '<regexp>' $(git rev-list --all)

If you run into an "Argument list too long" error:

    git rev-list --all | xargs git grep '<regexp>' 

If you want to limit the search to some subtree (for instance, "lib/util"), you will need to pass that to the rev-list subcommand and grep as well:

    git grep '<regexp>' $(git rev-list --all -- lib/util) -- lib/util
