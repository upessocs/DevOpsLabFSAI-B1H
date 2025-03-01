

# LAB-2 GIT COMMANDS
*BRANCHING*


Create a file and do 3 commits in it
### 1st change
```bash
git add .
git commit -m "version1"
```
![alt text](./assets/1.png)

### 2nd change
```bash
git add .
git commit -m "version2"
```
![alt text](./assets/2.png)

### 3rd change
```bash
git add .
git commit -m "version3"
```
![alt text](./assets/3.png)



View all commits by using git log

```bash
git log
```
![alt text](./assets/git_log.png)




```bash
git branch feature1
git log
```
![alt text](./assets/feature1.png)


CREATE NEW FILE AND ADD TWO COMMITS
```bash
git add.
git commit -m "feature commit 1"
```
```bash
git add.
git commit -m "feature commit 2"
```



![allcommit](./f7.png)

```bash
git checkout master
git log
```


![allcommit](./f8.png)


#Merging
```bash
git checkout feature1
git log

```

![allcommit](./f9.png)

Do the comit 3 in feature branch
```bash
git add .
git commit -m "feature done"
git log

```

![allcommit](./f10.png)

switching to master branch and perform merging
```bash
git checkout master
git merge feature1 -m "Merging featutre 1"
git log

```

![allcommit](./f11.png)

*RESET*
```bash
git reset --hard a462d13e9a
git log
``` 

*GIT RESET --HARD:Removed the merge commit 13dd279 and deleted all merged changes.*
*GIT RESET --SOFT:Would have removed the merge commit but kept changes staged, allowing you to re-commit easily.*

*REBASE*

```bash
git checkout feature1
git rebase master
git log
``` 

![allcommit](./f12.png)


