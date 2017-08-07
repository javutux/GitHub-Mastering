## GitHub-Mastering

### Setup

Before running git commands, we need:

git installed (preferably ≥ 2.0.0 as the default behavior for some commands has been greatly improved in late versions; see git 2.0.0 changelog)

### A git user i.e.:

```bash
a name git config --global user.name "My Name"
an email git config --global user.email "me@mail.org"
```

### Git Initialisation

 
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
 Creates a hidden repository to contain internal data.
 
 ### First commit
 
```bash
 $ git status
On branch master

Initial commit

nothing to commit (create/copy files and use "git add" to track)

$ echo "A dummy app listing ways to just say 'hello'" > README.md

$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md

$ git add README.md

$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

  new file:   README.md

$ git commit -m "First commit"
[master (root-commit) 45de2f7] First commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

$ git status
On branch master
nothing to commit, working directory clean
```

Note that at each step, the ```bash git status ```command provides helpful overview of the current repository state and a contextual help.

After this is done, you can also get Git via Git itself for updates:

```bash
$ git clone git://git.kernel.org/pub/scm/git/git.git
```

### Useful comands to change files

 ```bash 
 git add  
 ```
to add a new file or some modification in an already tracked file; the --patch option allows to select hunks only

```bash
git rm 
```
to remove a file from tracking

```bash
git mv
 ``` to rename a file
