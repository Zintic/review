Q: refusing to merge unrelated histories

A: 这是因为远程仓库已经存在代码记录了，并且那部分代码没有和本地仓库进行关联，我们可以使用如下操作允许pull未关联的远程仓库旧代码：--allow-unrelated-histories


Q: 如何使用ssh的方式推送，拉取代码？
A: 
- 检查是否有公钥
```bash
ls ~/.ssh
```
- 寻找一对文件，一个类似id_dsa或id_rsa，即私钥；与之对应的是.pub文件，即公钥。
- 如果不存在上述文件，ssh-keygen生成

- 发送公钥.pub至管理员

完成上述操作，即完成了ssh访问
