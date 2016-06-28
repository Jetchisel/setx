# setx - A bash script than can be used for debugging another shell script.

https://github.com/Jetchisel/setx

Copyright 2016 Jetchisel

A bash shell script that inserts set [-+]x and a PS4 debug code
or a trap  to make  the script  execute  line by  line by using 
the return key.  Shell script is  more  verbose  when  the code
is  added  in the script in question. This script  requires the 
following GNU utilities, ed(1) for editing the shell script and
file(1)  for  testing  file type of the script in question  and
grep for matching patterns against the debug codes.


## Usage:
```
setx [OPTION]... [FILE]
```

## Options:
```
  -h    Show this help.
  -a    Show a brief info about setx.
  -b    Insert `set -x' or with a `PS4' at a specific line, requires numeric argument
  -e    Insert `set +x' in a specific line, requires a numeric argument.
  -u    Remove all the `debug' code, requires a file as an argument.
  -x    Add `set -x' code to the second line by default, requires a file as an argument.
  -X    Add `set -x' and a `PS4' code at the second line. by default, requires a file 
        as an argument.
  -p    Print all the `debug' codes from file.
  -s    Make the execution of the script line by line, defaults to the second line.
        Requires a file as an argument.
```

## Examples:
```
setx -x FILE              Insert `set -x' at the second line of FILE.
setx -x FILE -b 5         Insert `set -x' at the fifth line of FILE.
setx -x FILE -b 5 -e 10   Insert `set -x' at the fifth line and `set +x' at the 10th.
setx -X FILE              Insert `set -x' and a `PS4' at the second line of FILE.
setx -X FILE -b 5         Insert `set -x' and a `PS4' at the fifth line of FILE.
setx -X FILE -b 5 -e 10   Insert `set -x' and a `PS4' at the fifth line and `set +x' 
                          at the 10th.
setx -s FILE              Insert a trap at the second line of FILE.
setx -s FILE -b 5         Insert a trap at the fifth line of FILE.
setx -p FILE              Print the debug codes if found in FILE.
setx -u FILE              Remove all the debug code in FILE.

```

## TODO:
Add option to show carriage returns, trailing white spaces and option to delete it too.
Bring back long options! (maybe :))


For more info about debugging please have a look at the following site.

https://www.shellcheck.net

http://mywiki.wooledge.org/BashGuide/Practices#Debugging

