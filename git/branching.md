# git branching

Sometimes you may not be sure that you want to directly commit your changes
directly to the line of work, like in case where you want to add a feature, but
you are not sure that your changes might end up, and also you don't want to mess
up the main line of work. So instead you use branches.

A _branch_ a shallow copy of your current branch (like a tree) on which you can
work on. When you are satisfied with your changes on a branch, you can merge
that branch back into your main branch. This main branch is usually labelled
`master`.

![git branches](https://git-scm.com/book/en/v2/images/advance-master.png)


## The `HEAD` pointer

The `HEAD` pointer points to the location where your commits end up. By moving
this `HEAD` pointer, you can switch between branches and also move to different
location in your commit tree.

### Listing branches

``` bash
$ git branch
```


### Creating branches

To create a branch on your local machine and switch in that branch

``` bash
$ git checkout -b [name_of_your_new_branch]
```


### Moving between branches

``` bash
$ git checkout [name_of_your_new_branch]
```


### Deleting braches

Delete a branch on your local filesystem:

``` bash
$ git branch -d [name_of_your_new_branch]
```

To force the deletion of local branch on your filesystem:

``` bash
$ git branch -D [name_of_your_new_branch]
```


### Merging branches
``` bash
$ git checkout master
$ git merge iss53
```

Before merging:
![before merging](https://git-scm.com/book/en/v2/images/basic-merging-1.png)

After merging:
![after merging](https://git-scm.com/book/en/v2/images/basic-merging-2.png)
