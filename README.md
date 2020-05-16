---
title: About
---
[![Build Status](https://travis-ci.com/hqweay/my-mkdocs.svg?branch=master)](https://travis-ci.com/hqweay/my-mkdocs) [![GitHub repo size](https://img.shields.io/github/repo-size/hqweay/my-mkdocs.svg)](https://github.com/hqweay/my-mkdocs.git)

# MkDocs

Hi! This is Hqweay's Wiki, powered by [https://www.mkdocs.org/](https://www.mkdocs.org/) and theme [mkdocs-material](https://github.com/squidfunk/mkdocs-material) , hosted on Github Pages, built by [https://travis-ci.com/](https://travis-ci.com/) .

You can find me on:

* Blog : [https://leay.net](https://leay.net)

## Full Text Search

If you want the full text search by chinese or other asia languages on mkdocs sites, add the next line on your `mkdocs.yml`.

```yml
extra:
  search:
    language: 'en, ja'
```

## Travis CI

Add `.travis.yml` just like this :

```yml
language: python

branches:
  only:
    - master

install:
- pip install mkdocs
- pip install mkdocs-material

script:
  - git clean -f -d -x
  - mkdocs build
  - mv site/* .

deploy:
  provider: pages
  skip_cleanup: true
  target_branch: gh-pages
  token: $GITHUB_TOKEN
  keep_history: true
  on:
    branch: master
```

Remeber to configurate `$GITHUB_TOKEN` on your repository setting in [https://travis-ci.com/](https://travis-ci.com/) .

Actually I don't know what's the perfect configuration, but this works for me...