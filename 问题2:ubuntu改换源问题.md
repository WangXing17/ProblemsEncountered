# ubuntu下载ipython3 或其他软件时出现Unable to locate package问题，或者下载较慢问题，需要换成国内的源   

1. 对source.list文件进行备份   
  `sudo cp /etc/apt/sources.list /etc/apt/sources.list_backup`
2. 编辑source.list文件，将软件源添加到文件前面中，如阿里云的源    
  `xw@ubuntu:/etc/apt$ sudo gedit sources.list`   
  deb-src http://archive.ubuntu.com/ubuntu xenial main restricted #Added by software-properties   
  deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted    
  deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted multiverse universe #Added by software-properties    
  deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted    
  deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted multiverse universe #Added by software-properties    
  deb http://mirrors.aliyun.com/ubuntu/ xenial universe   
  deb http://mirrors.aliyun.com/ubuntu/ xenial-updates universe   
  deb http://mirrors.aliyun.com/ubuntu/ xenial multiverse   
  deb http://mirrors.aliyun.com/ubuntu/ xenial-updates multiverse   
  deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse    
  deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse #Added by software-properties    
  deb http://archive.canonical.com/ubuntu xenial partner    
  deb-src http://archive.canonical.com/ubuntu xenial partner    
  deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted   
  deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted multiverse universe #Added by software-properties   
  deb http://mirrors.aliyun.com/ubuntu/ xenial-security universe    
  deb http://mirrors.aliyun.com/ubuntu/ xenial-security multiverse    
3. 使修改生效
  `xw@ubuntu:/etc/apt$ sudo apt-get update`   
  
  
国内其他附加源：    
  1. 清华源：    
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse   
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse   
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse   
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse   
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse   
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse   
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse    
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse    
  deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse    
  deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse      
  2. 中科大：   
  deb https://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse    
  deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse    
  deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse    
  deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse    
  deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse    
  deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse    
  deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse   
  deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse   
  deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse   
  deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse   
  3. 163源：    
  deb http://mirrors.163.com/ubuntu/ bionic main restricted universe multiverse   
  deb http://mirrors.163.com/ubuntu/ bionic-security main restricted universe multiverse    
  deb http://mirrors.163.com/ubuntu/ bionic-updates main restricted universe multiverse   
  deb http://mirrors.163.com/ubuntu/ bionic-proposed main restricted universe multiverse    
  deb http://mirrors.163.com/ubuntu/ bionic-backports main restricted universe multiverse   
  deb-src http://mirrors.163.com/ubuntu/ bionic main restricted universe multiverse   
  deb-src http://mirrors.163.com/ubuntu/ bionic-security main restricted universe multiverse    
  deb-src http://mirrors.163.com/ubuntu/ bionic-updates main restricted universe multiverse   
  deb-src http://mirrors.163.com/ubuntu/ bionic-proposed main restricted universe multiverse    
  deb-src http://mirrors.163.com/ubuntu/ bionic-backports main restricted universe multiverse   
