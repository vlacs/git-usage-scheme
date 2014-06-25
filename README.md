# VLACS git usage scheme
This is a description of how various VLACS libraries use git to manage code.

This is based off of this page:
http://nvie.com/posts/a-successful-git-branching-model/

## Primary branches
There are two primary branches
    - ```prod```
    - ```dev```

These respective branches desribe exactly what they are. ```prod``` is the most
stable version of the library or applications where ```dev``` is your latest,
greatest, bleeding-edge code that exists.

## Secondary branches
There may be many secondary branches which consist of two types:
    * Feature branches
    * Hotfix branches

These branches will be prefixed ```f/some-feature-name``` and
```h/some-hotfix-name```. Features are intended to be changes in the application
that are non-critical. Hotfixes are intended to be changes that need to be put
into production immediately such as bugs that prevent users from doing
something. 

## What branches should merge into others?
```prod``` should merge into ```dev``` or ```hotfix``` branches.

```dev``` should merge into ```feature```, ```hotfix```, or ```prod``` branches.

```hotfix``` branches should merge into ```dev``` or ```prod```.

```feature``` branches should merge only merge into ```dev```.

