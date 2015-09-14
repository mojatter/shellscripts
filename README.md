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
$ for i in {0..4}; do echo $i >>/tmp/test.log; done
$ ./recat /tmp/test.log
0
1
2
3
4
$ for i in {5..9}; do echo $i >>/tmp/test.log; done
$ ./recat /tmp/test.log -n 2
5
6
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

## dockerfile2sh

Output sh scripts from Dockerfile

```
Usage:
perl dockerfile2sh [Dockerfile]
```
