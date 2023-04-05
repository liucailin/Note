国内yum install会太慢 推荐采用国内的yum源，下面是采用aliyun



1. 备份   CentOS-Base.repo
2.  替换 curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
3.  yum clean all 
4. yum makecache