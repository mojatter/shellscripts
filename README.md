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
$ echo $'01\n02\n03\n04\n05' >/tmp/test.log
$ ./recat /tmp/test.log
01
02
03
04
05
$ echo $'06\n07\n08\n09' >>/tmp/test.log
$ ./recat /tmp/test.log -n 2
06
07
```

## memcached-keys

A simple code like memcached-tools.

moved from
https://code.google.com/p/memcached-keys/

```
Usage:
perl memcached-keys [host:port] ([prefix])
```

Example

```
perl memcached-keys
perl memcached-keys localhost:11211
perl memcached-keys localhost:11211 member
perl memcached-keys | sort >sorted-keys.txt
```
