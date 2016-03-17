# shell scripts

## recat

"recat" utility reads file, writing them to the standard output and keeps line position.

```
Usage: recat [OPTION] FILE
Options:
  -n [number]  lines
```

Example

```
$ for i in {0..4}; do echo "i $i" >>/tmp/test.log; done
$ ./recat /tmp/test.log
i 0
i 1
i 2
i 3
i 4

$ for i in {5..6}; do echo "i $i" >>/tmp/test.log; done
$ ./recat /tmp/test.log -n 2
i 5
i 6
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
