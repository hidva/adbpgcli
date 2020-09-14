FROM centos:7

MAINTAINER adbpg <adb-pg@list.alibaba-inc.com>

RUN \
mkdir -pv /tmp/adbpgcli-workspace/adbpg4cli && \
cd /tmp/adbpgcli-workspace/adbpg4cli  && \
curl -s -o adbpg4.tar.gz 'http://docs-aliyun.cn-hangzhou.oss.aliyun-inc.com/assets/attach/43729/cn_zh/1491914523043/apsaradb_for_gp_client_package.redhat.el7.x86_64.tar.gz?spm=a2c4g.11186623.2.25.7ef62723dZJzir&file=apsaradb_for_gp_client_package.redhat.el7.x86_64.tar.gz'    && \
tar -xzvf adbpg4.tar.gz && \
mv -v ./apsaradb_for_gp_client_package /usr/local/adbpg4    && \
cd /    && \
rm -rvf /tmp/adbpgcli-workspace && \
cd /usr/local/adbpg4/bin && \
for tool in *; do ln -sv `pwd`/${tool} /usr/local/bin/${tool}; done 
