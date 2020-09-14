FROM centos:7

MAINTAINER adbpg <adb-pg@list.alibaba-inc.com>

RUN \
mkdir -pv /tmp/adbpgcli-workspace/adbpg6cli && \
cd /tmp/adbpgcli-workspace/adbpg6cli  && \
curl -s -o adbpg6.tar.gz 'http://docs-aliyun.cn-hangzhou.oss.aliyun-inc.com/assets/attach/181125/cn_zh/1598426198114/adbpg_client_package.el7.x86_64.tar.gz?spm=a2c4g.11186623.2.27.7ef62723dZJzir&file=adbpg_client_package.el7.x86_64.tar.gz'   && \
tar -xzvf adbpg6.tar.gz && \
mv -v ./adbpg_client_package /usr/local/adbpg6  && \
cd /    && \
rm -rvf /tmp/adbpgcli-workspace && \
cd /usr/local/adbpg6/bin && \
for tool in *; do ln -sv `pwd`/${tool} /usr/local/bin/${tool}; done
