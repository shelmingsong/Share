# 分享文件说明
## `areainfo.sql`
* **内容**：全国省市区县 MySQL 数据库，含行政区划编码、名称、父级行政区划编码。
* **来源**：基于国家统计局2017年3月发布数据（http://www.stats.gov.cn/tjsj/tjbz/xzqhdm/201703/t20170310_1471429.html ）自行制作
* **制作原因**：网上现有省市区县文件太旧，或是要收费。

## `CentOS-Base-USTC.repo`
* **内容**：中科大 Centos7 软件源 repo 文件。
* **来源**：http://mirrors.ustc.edu.cn/help/centos.html 正文文本的简单复制粘贴
* **制作原因**：方便直接使用shell脚本获取，可以通过以下shell脚本实现自动化部署：
```bash
#!/usr/bin/env bash

cd /etc/yum.repos.d/
wget https://raw.githubusercontent.com/shelmingsong/Share/master/CentOS-Base-USTC.repo
yum clean all
yum makecache
```

## `sources.list_ubuntu_18.04`
* **内容**：阿里云 Ubuntu 18.04 软件源 repo 文件。
* **来源**：https://opsx.alibaba.com/mirror 中 ubuntu 右侧帮助按钮点开后的正文文本的简单复制粘贴
* **制作原因**：方便直接使用shell脚本获取，可以通过以下shell脚本实现自动化部署：
```bash
#!/usr/bin/env bash

cd /etc/apt/
mv sources.list sources.list.back
wget https://raw.githubusercontent.com/shelmingsong/Share/master/sources.list_ubuntu_18.04
mv sources.list_ubuntu_18.04 sources.list
apt-get clean
apt-get update
```
