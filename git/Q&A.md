Q: refusing to merge unrelated histories

A: 这是因为远程仓库已经存在代码记录了，并且那部分代码没有和本地仓库进行关联，我们可以使用如下操作允许pull未关联的远程仓库旧代码：--allow-unrelated-histories