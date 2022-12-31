Windows 环境配置

1. 生成公私钥

```ssh
<!-- 针对每个项目文件，配置不同的账号管理配置 -->
cd /project
git config --local user.name "rudolphbrowne"
git config --local user.email "rudolphbrowne@mail.com"

<!-- 生成公私钥 -->
ssh-keygen -t rsa "rudolphbrowne@mail.com"

<!-- 查看生成的公私钥 -->
ls ~/
```

2. 添加公钥到 git网站 ssh keys

![](Snipaste_2023-01-01_01-45-33.png)

3. 添加私钥到对应账号

```ssh
eval $(ssh-agent -s)
<!-- Agent pid 27688 -->
ssh-add /c/Users/27688/.ssh/id_rsa_rudolphbrowne_github
```

4.配置密钥绑定的网站及账户

```
cd ~/.ssh
vim config
<!-- CV 下面的信息
Host github.com
User rudolphbrowne@mail.com
Hostname ssh.github.com
preferredAuthentications publickey
IdentityFile ~/id_rsa_rudolphbrowne_github
Port 443
-->

<!-- 测试访问 -->
ssh -T git@github.com
```
![](Snipaste_2023-01-01_01-58-39.png)

5. 拉取项目

```ssh
git clone git@github.com:rudolphbrowne/fragment.git
```
