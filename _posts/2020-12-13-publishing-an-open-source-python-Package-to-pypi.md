---
layout: post
title: "Publishing an Open-Source Python Package to PyPI"
categories: py
author:
- Yi Zhang
---

## Make Your Code Publish-Ready

```bash
.
└── pybackground
    ├── __init__.py
    └── scheduler.py

```



## Create The Files PyPI Needs

```bash
.
├── LICENSE
├── README.md
├── pybackground
│   ├── __init__.py
│   └── scheduler.py
└── setup.py
```



## Create a New Empty Repository on GitHub



## Upload  Your Files To GitHub

```
$ cd PyBackground
$ git init
$ git add *
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin git@github.com:yzhang-dev/PyBackground.git
$ git push -u origin main
```



## Create a Python Package

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



## Create an Account On PyPI

[**Register**](https://pypi.org/account/register/)



## Upload Your Package To PyPI

```bash
$ python -m twine upload dist/*
```



## Install Your Own Package Using pip

```bash
$ pip install PyBackground
```
