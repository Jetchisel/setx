# setx - Just another bash script than can be used for debugging another shell script.

https://github.com/Jetchisel/setx

Copyright 2016 Jetchisel

A bash  shell  script that  inserts  set -x and a PS4 debug code  right after the shebang.
A shell script is a bit more  verbose when the code is added after the shebang or hashbang
setx relies heavily on GNU ed(1) for editing the script in quetion and file(1) for testing
the file type of the script in question.

## Usage:
```
setx [OPTION] [FILE
```

## Options:
```
-i, --insert   Insert set -x and PS4 debug code below the shebang.
-d, --delete   Remove set -x and PS4 debug code below the shebang.
-h, --help     Show this help.
-a, --about    A brief info.
```

For more info about debugging please have a look at the following site.

https://www.shellcheck.net

http://mywiki.wooledge.org/BashGuide/Practices#Debugging

