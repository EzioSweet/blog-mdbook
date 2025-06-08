# 在WSL里安装Gentoo

## WSL

WSL即Windows Subsystem Linux，WSL是我们最简单最轻松体验和使用Linux的方式，大多数发行版在MS Store中都可以直接安装，如图所示

![](/assets/img/Linux/WSL_in_MSStore.png)

但是，由于Gentoo的更新非常频繁，很难维护一个在MS Store中随主流更新的WSL版本，因此我们需要手动下载WSL安装包，导入到WSL中使用

## Gentoo In WSL

首先我们访问[https://wsl.gentoo.zip/](https://wsl.gentoo.zip/)，这里是Gentoo WSL的存档点。

下载符合我们使用版本的.wsl文件

然后我们运行

```bash
wsl --install --from-file .\xxxx.wsl
```

这样就把Gentoo安装到我们的wsl里了

整体上流程非常简单，但是刚安装的系统实际上非常不完善，可能会有一些问题

> 问题  
> setlocale: unsupported locale setting

这个问题不是所有的都会出现的，但是不少都会出现

我们要做的是给我们的系统添加locale，具体步骤如下：

```bash
su -c "nano /etc/locale.gen"
```

取消对应区域的注释

```bash
su -c "locale-gen"
```

```bash
su -c "/etc/env.d/02locale" 
# 在文件中添加
LANG="en_US.UTF-8"
LC_COLLATE="C.UTF-8"
```

最后执行

```bash
su -c "env-update"
source /etc/profile
```

> 换源  
> 使用ustc源

编辑  /etc/portage/repos.conf/gentoo.conf  
添加

```bash
[DEFAULT]
main-repo = gentoo

[gentoo]
location = /usr/portage
sync-type = rsync
sync-uri = rsync://rsync.mirrors.ustc.edu.cn/gentoo-portage
auto-sync = yes
```

> sync 过程中巴拉巴拉报一堆错误  

这种情况一般是没有设置profile导致的

```bash
eselect profile list  
eselect profile set [id]
```

> 没有sudo权限

```bash
su -c "visudo"
su -c "gpasswd -a [username] wheel"
```