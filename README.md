pyjulia
=======

[![Build Status](https://travis-ci.org/JuliaLang/pyjulia.svg?branch=master)](https://travis-ci.org/JuliaLang/pyjulia)

Experimenting with developing a better interface to julia that works with Python 2 & 3.

to run the tests, execute from the toplevel directory

```shell
python -m unittest discover
```

**Note** You need to explicitly add julia to your PATH, an alias will not work.

`pyjulia` is tested against Python versions 2.7, 3.3 and 3.4.  Older versions of Python are not supported.

Installation
------------
You will need to install PyCall in your existing Julia installation

```
Pkg.add("PyCall")
```

Your python installation must be able to call Julia.  If your installer
does not add the Julia binary directory to your PATH, you will have to
add it.

Usage
-----
To call Julia functions from python, first import the library

```
import julia
```

then create a Julia object that makes a bridge to the Julia interpreter

```
j = julia.Julia()
```

You can then call Julia functions from python

```
j.sind(90)
```
