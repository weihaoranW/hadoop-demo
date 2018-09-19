这是我在本机作的虚拟机的配置环境测试kvm,以最真实在接近生产环境,测试hadoop的性能及工作横式,暂不考虑ND的单点故障问题.  
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
# 设置并配置hadoop以standlone模式运行,熟悉环境
下载程序:http://www.apache.org/dyn/closer.cgi/hadoop/common/
并解压至/opt/hadoop.   
cd /opt/hadoop/etc/hadoop/.   
vim hadoop-env.sh.   
更改JAVA_HOME的位置并保存.   
## 设置本机的ssh登录不需要口令.   
ssh localhost.   







