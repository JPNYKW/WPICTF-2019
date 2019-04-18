WPICTF web / chirp / 50pt

# About

#### This problem has an image.

![image](https://github.com/JPNYKW/WPICTF/blob/master/img/chal.jpg)

Other data is nothing. Only this one.  

# Wut i tried

1. Check meta-data, strings n binary.

First time, tried 3 commands.

```bash
$ exiftool chal.jpg
$ strings chal.jpg
$ binwalk -e chal.jpg
```

Couldn't find the flag.
