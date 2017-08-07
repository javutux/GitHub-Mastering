# GitHub-Mastering

## Setup

Before running git commands, we need:

git installed (preferably ≥ 2.0.0 as the default behavior for some commands has been greatly improved in late versions; see git 2.0.0 changelog)

### a git user i.e.:

```bash
a name git config --global user.name "My Name"
an email git config --global user.email "me@mail.org"
```

## Git Initialisation

 
```bash
 $ git init $HOME/bonjour
Initialized empty Git repository in /Users/marc/bonjour/.git/

$ cd $HOME/bonjour

$ tree -a -I hooks
.
└── .git
    ├── HEAD
    ├── config
    ├── description
    ├── info
    │   └── exclude
    ├── objects
    │   ├── info
    │   └── pack
    └── refs
        ├── heads
        └── tags
 ```
 
```bash
git init
```
just created a hidden repository to contain internal data.
 
 
 
After this is done, you can also get Git via Git itself for updates:

```bash
$ git clone git://git.kernel.org/pub/scm/git/git.git
```
