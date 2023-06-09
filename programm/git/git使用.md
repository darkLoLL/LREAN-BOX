# git

## 使用git前的配置

git自带一个 `git config`工具配置，通过命令可以查看所有的配置以及所在的文件

```bash
git config --list --show-origin
```

### git config 
配置用户信息，配置用户名和邮件地址，这一点是很重要的，每一个Git提交都会使用这些信息

```sh
git config --global user.name "dark loll"
git config --global user.email "darkloll@qq.com"
```



## git常用命令

```sh	
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]
```



```shell
start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects
```

# 工作流

## 1、集中式工作流

适用：个人、3-5人小团队，熟悉 Subversion

## 2、功能分布式工作流

以集中式工作流为基础，为各个新功能分配一个专门的分支来开发，适用：中型团队8-12人

## 3、Git Flow工作流

通过为功能开发、发布为准和维护分配的分支，让发布迭代过程更加流畅。适用：整合公司

## 4、Forking 工作流

是分布式工作流，充分利用了git在分支和克隆的优势，适用：跨国合作

p.s.

[[git flow工作流]]



