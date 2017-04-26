# Linux Tips


## Common 
###  Switch java/python version

Reference: http://www.bkjia.com/Pythonjc/1182486.html   
Or you can refer the man page of update-alternatives

- Add the alter configure
```
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2.7 1
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.5 2
```

- Remove the configure
```
sudo update-alternatives --remove python /usr/bin/python3.5
sudo update-alternatives --remove python /usr/bin/python2.7
```

- Alter the configure
  update-alternatives --config python

## Maven Usage

### Display the depence tree

    mvn dependency:tree

## Git Usage

### Undo all the local changes

    http://stackoverflow.com/questions/14075581/git-undo-all-uncommitted-changes


This will unstage all files you might have staged with git add:

    git reset

This will revert all local uncommitted changes (should be executed in repo root):

    git checkout .

You can also revert uncommitted changes only to particular file or directory:

    git checkout [some_dir|file.txt]

Yet another way to revert all uncommitted changes (longer to type, but works from any subdirectory):

    git reset --hard HEAD
This will remove all local untracked files, so only git tracked files remain:

    git clean -fdx

### Git skills

https://github.com/521xueweihan/git-tips    

### How to write a better commit message for git?

    https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message
    https://ruby-china.org/topics/15737
    https://www.zhihu.com/question/21209619?sort=created

An example:

```
Fix bug where user can't signup.

[Bug #2873942]

Users were unable to register if they hadn't visited the plans
and pricing page because we expected that tracking
information to exist for the logs we create after a user
signs up.  I fixed this by adding a check to the logger
to ensure that if that information was not available
we weren't trying to write it.
```

```
Redirect user to the requested page after login

https://trello.com/path/to/relevant/card

Users were being redirected to the home page after login, which is less
useful than redirecting to the page they had originally requested before
being redirected to the login form.

* Store requested path in a session variable
* Redirect to the stored location after successfully logging in the user
```


## Linux Command

### How to make ls show file size as megabytes?

    ls -l --block-size=M

Reference: http://unix.stackexchange.com/questions/64148/how-do-i-make-ls-show-file-sizes-in-megabytes


###  How to use top to show threads within on process?

    top -H -p <pid>

For more usage information about __top__ , refer to the __top__ man page.


