# Git commands
A list of the most commonly used git commands

#### Cloning
```
$ cd /chosen-path/
```

```
$ git clone [project URL]
```

##### If you want to do a shallow clone which would only get the recent commit and ignore all of it's history you can do

```
$ git clone [project URL] --depth=1
```

#### Adding/committing and pushing

```
$ git add [directory]

$ git commit -m 'your commit message'

$ git push 
```


#### Creating a new branch
```
$ git checkout -b [branch-name]
```

#### Pushing your branch to repo for the first time
```
$ git push -u origin [branch-name]
```

#### Switching branch
```
$ git checkout [branch-name]
```

#### To see a list of all your branches 
```
$ git branch
```

#### To delete a branch
Make sure you're not on the branch you want to delete otherwise it will not work
```
$ git branch -d [branch-name]
```

#### This pulls your branch from origin if you do not have it locally
```
$ git checkout -b [branch-name] origin/[branch-name]
```
#### Safely merging two branches
```
$ git merge [branch-name] --no-commit --no-ff
```
(the --no-commit does not automatically commit the branch after merging and --no-ff does not fast forward the branch you're merging into)

#### Solving conflicts
```
$ git checkout --theirs /path-to/conflict-file 
````
(this will check out their file if you know your local one is outdated)

```
$ git checkout --ours /path-to/conflict-file
```
(this will check out your file if you know the one in the repository is outdated)

Otherwise, you'll have to manually sort through them in the conflicted file. Make sure you have no <<< or >>> in your file as your conflicts live in these.

#### Reverting

If you want to delete your current changes and revert back to the previous commmit 
```
$ git reset --hard
```
#### Show a log of your recent commits
```
$ git log
```