# GIT

## ADD
To add files in git you can run
```
git add filename
```
If you want to add all files which are uncommited
```
git add *
```
If you want to add hidden files also run
```
git add .
```

## COMMIT
To commit the current changes
```
git commit
```
this will open a editor (nano/vim) based on your system you can add commit message there
```
git commit -m "<your commit message>"
```


```
git add .
git commit -m "<my message>"
```
is same as 
```
git commit -a -m "<my message>"
```

(in case of merge conflicts dont use personal commit message)


## PUSH
To push your current commits
```
git push
```

for particular branch use
```
git push <repo alias> <branch name>
```
EX: ``` git push origin master```

## PULL
To pull commits from remote repo (Ex: from github)
```
git pull
```

to pull from particular branch
```
git pull <repo alias> <branch name>
```
EX: ``` git pull origin master```
