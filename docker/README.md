centos7 install docker
requirements: kernel >= 3.10
1. make sure yum latest  
yum update

2. remove docker if already installed  
yum remove docker  docker-common docker-selinux docker-engine  

3. install packages (yum-utils provide yum-config-manage, device-mapper-persistent-data & lvm2 provide devicemapper)  
yum install -y yum-utils device-mapper-persistent-data lvm2

4. set yum repo  
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

5. list docker versions in repo  
yum list docker-ce --showduplicates | sort -r

6. install  
yum install docker-ce

7. boot up  
systemctl enable docker

8. start  
systemctl start docker



