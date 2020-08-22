FROM centos:7.5.1804
RUN  yum update -y && yum upgrade -y \
    && yum -y install git
RUN cd \
&& git clone https://github.com/tagomoris/xbuild.git \
&& mkdir local \
&& xbuild/go-install 1.10.3 $HOME/local/go

ENV PATH /root/local/go/bin:/root/go/bin:/local/go/bin:/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
#ENV PATH $HOME/local/go/bin:$HOME/go/bin:$PATH 
#export PATH=$HOME/local/go/bin:$HOME/go/bin:$PATH

  #&& yum install golang -y \
  #&& yum install nginx -y \
  #&& yum install mariadb-server -y

RUN yum install -y make \
&& yum install -y mariadb-server mariadb mariadb-client