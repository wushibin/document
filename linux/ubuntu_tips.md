# Ubuntu Tips

### Set the display on ubuntu

Reference: http://blog.csdn.net/neosmith/article/details/42076331

```shell
#!/bin/bash  
  
xrandr --newmode "1920x1080_60.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync  
xrandr --addmode VGA1 "1920x1080_60.00"  
```

### Enable the root user

https://askubuntu.com/questions/44418/how-to-enable-root-login