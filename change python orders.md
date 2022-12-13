## How to change python version default in Ubuntu 20.04 

1. Check the installed versions of Python:

```
$ ls /usr/bin/python*

```

2. Then, create the alternatives:

```
$ sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 1
$ sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 2

```

3. Then, choose the version you want:

```
$ sudo update-alternatives --config python

```
