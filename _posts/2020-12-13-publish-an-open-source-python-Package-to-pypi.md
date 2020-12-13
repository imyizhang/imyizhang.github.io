---
layout: post
title: "Publish an Open-Source Python Package to PyPI"
categories: py
author:
- Yi Zhang
---

## Make your code publish-ready

```bash
.
├── pybackground
    ├── __init__.py
    └── scheduler.py

```





## Create the files PyPI needs

```bash
.
├── LICENSE
├── README.md
├── pybackground
│   ├── __init__.py
│   └── scheduler.py
└── setup.py
```



## Create a new empty repository on GitHub



## Upload  your files to GitHub

```
$ cd PyBackground
$ git init
$ git add *
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin git@github.com:yzhang-dev/PyBackground.git
$ git push -u origin main
```



## Create a Python package

```bash
$ pip install --upgrade setuptools wheel twine
```



```bash
$ python setup.py sdist bdist_wheel
```



```bash
.
├── LICENSE
├── PyBackground.egg-info
│   ├── PKG-INFO
│   ├── SOURCES.txt
│   ├── dependency_links.txt
│   └── top_level.txt
├── README.md
├── build
│   ├── bdist.macosx-10.9-x86_64
│   └── lib
│       └── pybackground
│           ├── __init__.py
│           └── scheduler.py
├── dist
│   ├── PyBackground-0.1.0-py3-none-any.whl
│   └── PyBackground-0.1.0.tar.gz
├── pybackground
│   ├── __init__.py
│   └── scheduler.py
└── setup.py
```



## Create an account on PyPI

[Regiter](https://pypi.org/account/register/)



## Upload your package to PyPI

```bash
$ python -m twine upload dist/*
```



## Install your own package using pip

```bash
$ pip install PyBackground
```
