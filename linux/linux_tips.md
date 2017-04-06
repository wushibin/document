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



## Linux Command

### How to make ls show file size as megabytes?

    ls -l --block-size=M

Reference: http://unix.stackexchange.com/questions/64148/how-do-i-make-ls-show-file-sizes-in-megabytes


###  How to use top to show threads within on process?

    top -H -p <pid>

For more usage information about __top__ , refer to the __top__ man page.


