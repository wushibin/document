# Linux Tips

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