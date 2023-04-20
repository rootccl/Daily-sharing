# VMware

### 网络

第一次安装Centos系统后，无法联网，测试如下：

```shell
curl www.baidu.com
```

出现这种curl请求失败的情况，可以修改配置来解决

```shell
cd /etc/sysconfig/network-scripts
vim ifcfg-ens33
```

将"ONBOOT=no"修改为"ONBOOT=yes"

```shell
service network restart
```



### tab键bibi声音

在VMware中按tab键自动补全的时候，经常会出现bibi声音，可以通过修改配置来消除：

打开虚拟机系统存放的目录，找到系统的\*.vmx文件，使用记事本编辑，在文件中加上以下一行：

mks.noBeep = "TRUE"

保存后，重新打开，OK！
