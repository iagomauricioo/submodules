# Forma correta de criar submodules
### Repositórios como esse podem ser utilizados para fazer Multirepos de Microsserviços
Pode ser clonado de forma completa com: ```git clone --recursive <url>```

```
$ mkdir git-submodule-demo
$ cd git-submodule-demo/
$ git init
Initialized empty Git repository in /Users/atlassian/git-submodule-demo/.git/
```
```
$ git submodule add https://bitbucket.org/jaredw/awesomelibrary
Cloning into '/Users/atlassian/git-submodule-demo/awesomelibrary'...
remote: Counting objects: 8, done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 8 (delta 1), reused 0 (delta 0)
Unpacking objects: 100% (8/8), done.
```


```
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

 new file:   .gitmodules
 new file:   awesomelibrary
```

```
$ git add .gitmodules awesomelibrary/
$ git commit -m "added submodule"
[main (root-commit) d5002d0] added submodule
 2 files changed, 4 insertions(+)
 create mode 100644 .gitmodules
 create mode 160000 awesomelibrary

git push origin main
```
