# xtools

Useful shell scripts

## recat

"recat" utility reads file, writing them to the standard output and keeps line position.

```
Usage: recat [OPTION] FILE
Options:
  -n [number]  lines
```

Example

```
$ echo $'1\n2\n3\n4\n5' >/tmp/test.log
$ ./recat /tmp/test.log
1
2
3
4
5
$ echo $'6\n7\n8\n9\n10' >>/tmp/test.log
$ ./recat /tmp/test.log -n 2
6
7
```
