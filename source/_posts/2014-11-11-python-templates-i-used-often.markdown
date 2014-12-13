---
layout: post
title: "python templates I used often."
date: 2014-11-11 10:59:37 +0800
comments: true
categories: 
---

command line input parser

``` python
def parse_sys_argv(argv):
    import argparse

    parser = argparse.ArgumentParser(description=
                                     'Please add description here.')
    parser.add_argument('argname')
    args = parser.parse_args(argv)
    return args

if __name__ == '__main__':
    import sys
    args = parse_sys_argv(sys.argv[1:])
```

* utf-8 source code encoding

```# -*- coding: utf-8 -*-
```