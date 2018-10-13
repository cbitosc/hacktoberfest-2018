# `git` working

A git _"repo"_ is a directory which may contain any type of files, may it be
your code or anything. git can be used to make snapshots of your code at any
given time. That instance is called a _"commit"_. These commits can then be used
to go back to a specific instance of your repo.


## Initializing a git repo

For a directory to become a git repository, you have to tell git to initialize
the repo using the `git init` command.

Create a new directory in your computer, open a terminal inside it and run

``` bash
$ git init
```

Now git starts tracking the changes in your repo.


## The `diff`

git, while making a commit only keeps track of the data that is changed from the
previous commit. It makes something called a _"delta"_(a "diff", difference) and
stores only that change in data.

Information about the repo is stored inside a hidden directory named `.git`
inside your directory.

## States of files in a repo

Files inside your repo will be in one of the there stages
1. Working
2. Staging
3. Commited

The state of files decide how the files are treated by git.


### 1. Working stage

By default when you add a file or directory to your repo it is in an _untracked_
stage. These files when you make a commit are not kept track of and won't be
considered as a part of the repo. Files that haven't been modified since the
previous commit are also considered to be in working area.


### 2. Staging area

For a file to be tracked by git it has to be said to keep track of it. Run

``` bash
$ git add /path/to/file
```

so that git starts keeping track of the files. When a file that is being tracked
is modified then it moves into an _untracked_ state where the changes will not
be considered. The above command had to be run again to move the files into
staging area. Files only inside the staging area are added the next commit.


### 3. Committed stage

And when you are finally ready with your changes, you _commit_ the changes.

``` bash
$ git commit
```

A _commit message_ needs to be specifing information about the commit. It can be
specified using the `-m` flag.

``` bash
$ git commit -m "commit message"
```

![git stages](https://git-scm.com/book/en/v2/images/areas.png)


> All the repo information is stored in the `.git` directory.
> For a beginner, you don't have to worry about the `.git` directory unless you
> have some serious business to do


### Downstream and Upstream
Your local repository is called a _downstrean_ repo. When you connect a repo to
another through a _remote_ to a different repo called an _upstream_. This is
also same for the the remote repository too. Changes made in one stream is not
refleced in another stream. It has to be _pushed_ to upstream and the same goes
got a _pull_. A repo can have multiple _remotes_ and each is named.

``` bash
# update remote repo reflecting local changes
$ git push <remote_name>

# update local repo reflecting rmeote changes
$ git pull <remote_name>
```

The remote name is optional for a _pull_.

[Next -> Branching](branching.md)
