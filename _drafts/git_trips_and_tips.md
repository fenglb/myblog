1. Git 恢复和回退的一些操作。

    a. 文件修改回撤。`git checkout -- <filename>`会回撤到INDEX STAGE或者HEAD。
    b. 文件删除回撤。如果直接用rm删除，`git checkout -- <filename>`；如果用`git rm <filename>`删除，就需要先`git reset <fjlename>`然后在用`git checkout -- <filename>`才能完全回撤。
    c. 修改最近一次提交的comments。`git commit --amend`, `git commit --amend -m "new comemnt"`。
    d. 回到到其他commit。`git reset --hard commit_id`。

补充说明，Git内的任何commit都会在`git reflog`内记录， 有很多操作也是更换了commit_id的，比如`git commit --amend`。所以如果你需要回退到之前操作过的一些版本，可以从这里面找到commit_id，然后用`git reset`回退到这个版本，但仅对于commit的内容有效。

2. `git tag`的用法。

`git tag -a 1.0.0 -m "comments"`，这个相当于在这个地方做一个tag，方便于以后回退和发布。比如您需要回退只需要`git checkout 1.0.0`就可以了。
