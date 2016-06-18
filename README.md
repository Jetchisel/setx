# setx - Just another bash script than can be used for debugging another shell script.

https://github.com/Jetchisel/setx

Copyright 2016 Jetchisel

A bash shell  script that  inserts set -x and a PS4 debug code  right after the shebang.
Shell script is a bit more verbose when the the code is added after the shebang or hashbang
setx relies heavily on GNU ed(1) and file(1).

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

