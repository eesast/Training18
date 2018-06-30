# Linux

- [Cloud Server](#cloud-server)

- [WSL](#wsl)

- [Virtual Host](#virtual-host)

## Cloud Server

云服务器，即非本地的，通过远程连接进行操作的 Linux 服务器。

### 简介

云服务器由于部署在云端，可以很方便地创建、修改和删除，以及备份、扩容等。

常见的云服务器提供商有 `阿里云`、`Azure`、`AWS`、`Google Cloud` 等，它们提供多种多样的云服务器，比如计算型、存储型等。

除此之外，还有一些运营商以提供优惠的个人虚拟主机 `VPS` 而出名，如 `Linode`、`DigitalOcean`、`BandwagonHost` 等，当然它们也提供商用方案。

### 获取

通过注册登录相应的运营商，我们可以选择云服务器的 `系统`、`物理部署地点`、`磁盘容量与内存大小` 等，并即时创建。

不同运营商的服务器配置方式不尽相同，这里不再详细说明。

### 使用

云服务器提供商一般会在服务器管理界面提供一个直连服务器的界面 `shell`，但我们往往通过本地的远程软件来登录服务器进行操作。

这里使用 `putty` 和 `WinSCP` 作为例子，讲解相关操作，其他软件使用方式相当类似，不再赘述。

1.  打开 `putty`，在 `Host Name` 中输入服务商提供的 `主机 IP`，端口号默认为 `22`（可修改），选择连接方式为 `SSH`，并在左侧菜单 `Connection - SSH - Auth` 中的 `Private key file for authentication` 选择与创建服务器使用的私钥匹配的公钥文件（可选）。

2.  点击 `Open`，在弹出的缓存提示中选择 `Yes`，连接上 `SSH`。

3.  在 `login as` 后输入你默认登录的用户名，如 `root`，并输入密码后回车（使用密钥文件则不需要输入密码）。

## WSL

`WSL` 全称为 `Windows Subsystem for Linux`，是微软提出的可在 Windows 下运行的 Linux 环境，支持大部分 Linux 应用程序。

### 简介

参考 👉[Windows Subsystem for Linux](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux)

### 获取

1.  确保系统版本是 `Windows 10 build 16215 或更高`，其他 Windows 10 版本的获取方法请参考 👉[Install using lxrun](https://docs.microsoft.com/zh-cn/windows/wsl/install-win10#for-anniversary-update-and-creators-update-install-using-lxrun)。`非 Windows 10 系统` 均不受支持。

2.  打开 `Windows 应用商店`，搜索 `Ubuntu`，这里选择安装 `Ubuntu 18.04`。其他 Linux 发行版可以自行尝试。

3.  安装完毕后，打开 `Ubuntu 18.04`，此时可以看到提示，`WSL 支持未开启`。此时可以通过在管理员权限的 `PowerShell` 里输入 `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux` 或在 `添加或关闭 Windows 功能` 中 `打开 WSL 支持`，最后根据提示重启。

4.  再次打开 `Ubuntu 18.04`，等待安装完成，输入你需要的用户名，再输入两次密码，完成账户设置。

### 使用

通过打开 `Ubuntu 18.04` 或在 `PowerShell` 中输入 `bash` 来再次进入 `WSL`。

## Virtual Host

配置 Linux 虚拟机环境，适合需要完整系统的情况。

### 获取

Windows 下一般使用 `VMWare Workstation` 和 `Oracle Virtual Box` 作为虚拟机，支持几乎所有 Linux 发行版镜像。

macOS 下有 `Parallels Desktop`、`VMware Fusion` 和 `Oracle Virtual Box`。

1.  安装虚拟机软件，除 `Oracle Virtual Box` 是免费软件外，其他软件需要正版授权，但功能和性能更强大。

2.  下载合适的 Linux 发行版镜像，推荐渠道：官网、[TUNA 源（清华大学开源软件镜像站）](https://mirrors.tuna.tsinghua.edu.cn/)右侧的 `获取下载链接`。

3.  添加和安装虚拟机，几乎所有虚拟机都支持 Linux 系统的快速安装，需要自定义时请关闭快速安装。

### 使用

合理利用虚拟机提供的暂停、快照等功能。
