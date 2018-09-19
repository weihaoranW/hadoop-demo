这是我的本机作的虚拟机的配置环境测试kvm
# 准备工作
准备四台虚拟机,以nat模式配置网络(以不影响网络上它机器的ip冲突)
ip及机器名分别为:
- debian-master-66 192.168.122.66   (NN)
- debian-master-67 192.168.122.67   (ND)
- debian-master-68 192.168.122.68   (ND)
- debian-master-69 192.168.122.69   (ND)  
每机分配1核cpu,1G内存.  
虚拟机上需要安装以下软件,有些已经具备****rsync,openssh-server**
dns,配置成宿主机的dns即可,否则,无法访问网络.  
配置java基本环境,ssh确保其中任一服务器之间可以免密码访问.  





    
