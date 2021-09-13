Git相关网上有非常多总结，在此放一个GitHub上的总结：
<br>https://github.com/huyaocode/webKnowledge/tree/master/%E5%AE%9E%E7%94%A8%E5%B7%A5%E5%85%B7%E4%B8%8E%E5%BA%93/Git

### 1. commit后重新回到上一个状态
+ git reset HEAD --soft &nbsp;&nbsp; 只回撤commit信息，如果想要提交，再次commit即可（推荐）
+ git reset HEAD --hard &nbsp;&nbsp; 将整个项目回撤到上一个版本，本地文件也会全部回撤（慎用）
+ git revert HEAD &nbsp;&nbsp; 撤销最近一次提交，产生一个新的提交，虽然代码回退了，但是版本依然是向前的

### 2. 分支操作
+ git branch xxxx &nbsp;&nbsp; 创建名为xxxx的分支
+ git branch &nbsp;&nbsp; 查看当前所处分支和各分支名
+ git branch -d xxxx &nbsp;&nbsp; 删除分支xxxx
+ git merge xxxx &nbsp;&nbsp; 合并分支xxxx
+ git branch -a &nbsp;&nbsp; 查看本地和远程所有分支
+ git branch -r &nbsp;&nbsp; 远程所有分支




