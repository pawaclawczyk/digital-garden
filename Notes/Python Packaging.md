---
title: "Python Packaging"
created-at: "2022-05-11 16:40"
public: true
language: en
tags: [idea]
---

# Python Packaging

Python has a build system defined in [PEP 517](https://peps.python.org/pep-0517/) and [PEP 518](https://peps.python.org/pep-0518/). There are frontends and backends for the build system.

[build](https://pypa-build.readthedocs.io/en/stable/) package is a PEP 517 compliant build frontend.

[setuptools](https://setuptools.pypa.io/en/latest/index.html) is used as the backend.

```toml
[build-system]  
requires = ["setuptools"]  
build-backend = "setuptools.build_meta"
```

