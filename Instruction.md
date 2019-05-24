# 这个仓库的使用
## 1. clone到你们本地或者你们的服务器路径下

```
git clone https://github.com/treatgut/TreatGutDocs.git
```

## 2. 让这个仓库识别你们

```
git config user.email "你的邮件"
git config user.name "你的github账户名"
```

## 3. 操作

你们可以修改你们想要修改的文件，添加或者删除。操作后再`push`,
比如我修改了文件`pythonDoc.md`就可以用`git status`看下我
修改的东西，确认无误后再`git add pythonDoc.md`,然后
`git commit pythonDoc.md "添加python使用"`进行操作记录备注
,接着再`git push`就可以推送修改到远程仓库了。

## 4. 远程仓库更新到本地

因为是团体的仓库，远程仓库很可能会被团体中的其他人更新，
所以我们可以先到远程仓库下看看做了哪些更新, 或者下载到
本地查看。然后再更新到本地，接着再进行你的开发。下面是
一种远程仓库更新到本地的方法。

```
# 先将远程仓库下载到本地并新建一个tmp分支
git fetch origin master:tmp
# 比较本地原来的分支与tmp分支的不同
git diff tmp
# 合并tmp分支到本地原来的分支
git merge tmp
# 删除tmp分支
git branch -d tmp
```

## 5. github 使用教程
上面是我知道的一些github的使用方法，具体你们可以参考如下：
+ [Learn Git Branching](https://learngitbranching.js.org/)
+ [Fork and Pull Request Workflow](https://github.com/susam/gitpr)

