# Git commands
A list of the most commonly used git commands

#### Cloning
Navigate into the folder you want to clone your project into

```
$ cd /chosen-path/
```
Then clone it

```
$ git clone [project URL]
```

##### If you want to do a shallow clone which would only get the recent commit and ignore all of it's history you can do

```
$ git clone [project URL] --depth=1
```


#### Checking git's status

Which files have changed, which branch is git using, etc

```
$ git status
```


#### Adding/committing and pushing

```
$ git add [file or directory]

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

#### Deleting a branch
Make sure you're not on the branch you want to delete otherwise it will not work

Delete a remote branch
```
$ git push origin --delete [branch-name]
```
Delete a local branch
```
$ git branch -d [branch-name]
```

#### This pulls your branch from origin if you do not have it locally
```
$ git checkout -b [branch-name] origin/[branch-name]
```
#### Safely merging a branch
Go onto the branch you want merge into, for example 'develop' then merge in your choosen branch for example 'kim-footer-amend' 
```
$ git merge [branch-name] --no-commit --no-ff
```
(the --no-commit does not automatically commit the branch after merging and --no-ff does not fast forward the branch you're merging into)

#### Solving conflicts
This will check out their file if you know yours is incorrect
```
$ git checkout --theirs /path-to/conflict-file 
````
This will check out your file if you know the one in the repo is outdated
```
$ git checkout --ours /path-to/conflict-file
```
Otherwise, you'll have to manually sort through them in the conflicted file. Make sure you have no `<<<` or `>>>` in your file as your conflicts live in these.

#### Reverting
If you want to delete your current changes and revert back to the previous commmit (this will lose any amends you haven’t commited so only do this if you're sure)
```
$ git reset --hard
```
#### Show a log of your recent commits
```
$ git log
```
