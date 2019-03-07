# ubuntu第一次使用vi出现按键错误

第一次使用ubuntu中的vi编辑文件时，出现了按上，下，左，右键时，会出现大写的A,B,C,D这种情况，按backspace（删除键）也失效了。   

![4_1.png](https://github.com/WangXing17/ProblemsEncountered/tree/master/images/4_1.png)    

解决方法如下：   
编辑/etc/vim/vimrc.tiny：   
由于/etc/vim/vimrc.tiny的拥有者是root用户，所以要在root的权限下对这个文件进行修改。   
1.很简单，这个文件里面的倒数第二句话是“set compatible”，将“compatible”改成“nocompatible”非兼容模式就可以解决方向键变ABCD的问题了。    
2.接下来要解决Backspace键的问题也很简单，在刚才那句话后面再加一句：set backspace=2    
如下图所示：   
![4_2.png](https://github.com/WangXing17/ProblemsEncountered/tree/master/images/4_2.png)    
