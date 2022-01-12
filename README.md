# Mac开发必备工具——Homebrew国内源

## 介绍

`Homebrew`是一款包管理工具，目前支持`macOS`和`Linux`系统。

由于官方提供下载地址，经常安装等待一段时间之后遇到下面提示

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

// 报错
curl: (7) Failed to connect to raw.githubusercontent.com port 443: Operation timed out
```

经过多次测试，发现`raw.githubusercontent.com`访问很不稳定，我们中国大陆用户访问的话经常容易访问不到其资源。

好奇为什么官方不通过`JSDelivr`等免费的CDN解决该问题？

所以在此基于官方的源码上修改其中`raw.githubusercontent.com`切换成中科大镜像，亲测速度还不错，哈哈放心食用。

## 快速安装

**JSDelivr**
```
/bin/bash -c "$(curl -fsSL https://cdn.jsdelivr.net/gh/qqlcx5/homebrew/install.sh)"
```
**码云**
```
/bin/bash -c "$(curl -fsSL https://gitee.com/qqlcx5/homebrew/raw/master/install.sh)"
```

## 卸载

**JSDelivr**
```
/bin/bash -c "$(curl -fsSL https://cdn.jsdelivr.net/gh/qqlcx5/homebrew/uninstall.sh)"
```

**码云**
```
/bin/bash -c "$(curl -fsSL https://gitee.com/qqlcx5/homebrew/raw/master/uninstall.sh)"
```

### 常用命令
* `brew help` 查看帮助
* `brew list` 列出已安装的软件包
* `brew install <package name>` 安装软件包
* `brew uninstall <package name>` 卸载软件包
* `brew search <package name>` 查找软件包
* `brew info <package name>` 查看软件包信息
* `brew -v` 查看`brew`版本
* `brew update` 更新`brew`
* `brew outdated` 列出需要更新的软件包
* `brew upgrade [<package name>]`可选指定更新某个软件包，默认更新所有软件包
