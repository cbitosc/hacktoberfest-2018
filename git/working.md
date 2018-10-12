# `git` working

A git _"repo"_ is a directory which may contain any type of files, may it be
your code or anything. git can be used to make snapshots of your code at any
given time. That instance is called a _"commit"_. These commits can then be used
to go back to a specific instance of your repo.


## Create a repo

Create a new directory in your computer, open a terminal inside it and run

``` bash
$ git init
```

Now git starts tracking the repo for changes. It's called a local repo because
its inside your local machine.


## The `diff`

git, while making a commit only keeps track of the data that is changed from the
previous commit. It makes something called a _"delta"_(a "diff", difference) and
stores only that change in data. Which means commits cannot be deleted randomly.

Information about the repo is stored inside a directory named `.git` inside your
directory.
