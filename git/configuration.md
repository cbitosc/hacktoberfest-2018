# Configuring `git`

`git` stores it configuration inside your home folder, in a file called
`.gitconfig` (note the period symbol in the filename is not a typo).

On Windows it's inside `C:\Users\<username>\` and on Unix based systems
`/home/<username>/`

> Installing through binaries on Windows might prompt you through a couple of
> settings, leave them to defaults unless you know what you are doing.

To edit the file open it with your favourite text editor. You find a couple of
entries in key value pairs formatted in
[`toml`](https://github.com/toml-lang/toml). You can edit it directly, but be
careful when you do so.

The recommended way to configure git is through the command line, using
`git config`.


## Basic configuration

The basic things to get done is to add your **name** and **email**, nothing can
go wrong right. Just run

``` bash
# adding name
$ git config --global user.name "Your name"

# adding email
$ git config --global user.email "address@server.com"
```

- [Advanced configuration ->](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)
- [Next -> Working of git](working.md)
