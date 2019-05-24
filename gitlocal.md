# git服务器

# 1. 创建git用户

服务器已经创建好了

```
groupadd git
useradd git -g git
```

# 2. 创建证书登陆

将所有开发人员需要登录的用户的公钥，公钥位于用户`home`目录下的`~/.ssh/id_rsa.pub`文件中，
把这些公钥导入到`/home/git/.ssh/authorized_keys`中。

# 3. 创建仓库

根据项目需要可以创建仓库,比如我在`/share/User/GitRepositories`目录下创建仓库

```
# cd /share/User/GitRepositories

# 初始化仓库 
git init --bare firsttest.git
# 添加该仓库的用户组
chown -R git:git firsttest.git

```

# 4. 克隆仓库

接下来就可以在本地

```
git clone git@ip:/share/User/GitRepositories/firsttest.git
#然后就可以进行开发
```
接下来的操作可以参考[Instruction](https://github.com/treatgut/TreatGutDocs/blob/master/Instruction.md)
