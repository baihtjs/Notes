# Kali渗透测试

## 任务1：Kali Linux渗透测试介绍

### 1、渗透测试标准

*   **PETS**
*   前期交互阶段
*   情报收集阶段
*   威胁建模阶段
*   漏洞分析阶段
*   渗透攻击阶段
*   后渗透测试阶段
*   渗透测试报告

### 2、渗透测试项目

*   渗透测试范围
*   获得授权
*   渗透测试方法：社会工程学&DDos

## 任务2：Kali Linux安装

### 1、Linux常用命令
* ps -ef
* ps aux
* top k
* tail /var/log/message
* watch -n 2 tail /var/log/message
* netstat -pantu
* netstat -pantu | awk '{print $4}'
* netstat -pantu | awk '{print $4}' | egrep -v 'ser | Local'
* netstat -pantu | awk '{print $4}' | egrep -v 'ser|oca|0.0.0.0'
* netstat -pantu | awk '{print $4}' | egrep -v 'ser|oca|0.0.0.0'| cut -d ':' -f 1
* netstat -pantu | awk '{print $4}' | egrep -v 'ser|oca|0.0.0.0'| cut -d ':' -f 1 | sort | uniq
* netstat -pantu | awk '{print $4}' | egrep -v 'ser|oca|0.0.0.0'| cut -d ':' -f 1 | sort | uniq >ip
* netstat -pantu | awk '{print $4}' | egrep -v 'ser|oca|0.0.0.0'| cut -d ':' -f 1 | sort | uniq >>ip
