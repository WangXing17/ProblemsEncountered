# 在用root用户进行git push origin master时遇到如下问题

![image](https://github.com/WangXing17/ProblemsEncountered/blob/master/images/1.png)

产生的原因：因为在生成ssh key的时候是用普通用户注册的，所有github上的公钥是和普通用户绑定的。但是没有和root用户绑定。

解决的方法：给root用户注册ssh key， 并绑定到github上。问题解决，步骤如下：
(1)生成 SSH KEY：  ssh-keygen -t rsa -C "782493798@qq.com"
(2)进入 /root/.ssh 目录，查看 id_rsa 和 id_rsa.pub 文件：
    root@localhost:~# cd /root/.ssh
    root@localhost:~/.ssh# ls -a
    root@localhost:cat id_rsa.pub
(3)将id_rsa.pub的内容复制到GitHub， Personal settings，SSH and GPG keys中。

参考：
(1)https://www.cnblogs.com/woider/p/6533709.html
(2)https://ask.csdn.net/questions/251624


