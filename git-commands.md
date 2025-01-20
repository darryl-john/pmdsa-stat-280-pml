# Setup global identity
```shell
$ git config --global --list
$ git config --global user.name "Darryl John"
$ git config --global user.email dvpagcaliwagan@dmcihomes.com
```

# Remote repository management 
```shell
$ git remote add origin https://github.com/OWNER/REPOSITORY.git
# Set a new remote

$ git remote -v
# Verify new remote
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
> origin  https://github.com/OWNER/REPOSITORY.git (push)
```

# Version Tagging
```shell
# Use tags to mark commits with version numbers:
$ git tag -a v2.5 -m 'Version 2.5'

# Push tags upstream—this is not done by default:
$ git push --tags

# Then use the describe command:
$ git describe --tags --long

# This gives you a string of the format:
v2.5-0-gdeadbee
^    ^ ^^
|    | ||
|    | |'-- SHA of HEAD (first seven chars)
|    | '-- "g" is for git
|    '---- number of commits since last tag
|
'--------- last tag
```

# Rebasing
```shell
$ git checkout dev
$ git rebase main 
```