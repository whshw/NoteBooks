# **Homebrew 使用笔记**

## **介绍**

[Homebrew](https://brew.sh/) 是一个包管理器，主要用于 macOS 和 Linux。它简化了软件安装过程，通过一个简单的命令可以安装、更新和删除软件包。

## **安装 Homebrew**

在安装 Homebrew 之前，确保已经安装了 Xcode Command Line Tools。可以通过以下命令安装：

```sh
xcode-select --install
```

然后，在终端中执行以下命令安装 Homebrew：

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

安装完成后，执行以下命令添加 Homebrew 到系统路径：

```sh
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/username/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## **使用 Homebrew**

### **搜索软件包**
可以使用 `brew search` 命令来搜索软件包：

```sh
brew search package_name
```

### **安装软件包**
使用 `brew install` 命令来安装软件包：

```sh
brew install package_name
```

例如，安装 `wget`：

```sh
brew install wget
```

### **更新软件包**

使用 `brew update` 命令来更新 `Homebrew` 自身以及已安装的软件包信息：

```sh
brew update
```

使用 `brew upgrade` 命令来更新所有已安装的软件包：

```sh
brew upgrade
```

### **卸载软件包**
使用 `brew uninstall` 命令来卸载软件包：

```sh
brew uninstall <软件包名>
```

例如，卸载 `wget`：

```sh
brew uninstall wget
```

### **查看已安装的软件包**
使用 `brew list` 命令来查看所有已安装的软件包：

```sh
brew list
```

### **查看软件包信息**
使用 `brew info` 命令来查看软件包的详细信息：

```sh
brew info <软件包名>
```

## **管理 `Homebrew` 插件**
`Homebrew` 支持通过插件扩展其功能。常用的插件包括 `brew cask` 和 `brew services`。

安装 `brew cask`
`brew cask` 用于管理 `macOS` 应用程序的安装。它已经集成在 `Homebrew` 中，无需单独安装。可以直接使用 `brew install --cask` 命令安装应用程序，例如：

```sh
brew install --cask google-chrome
```

### **管理服务**
`brew services` 插件用于管理作为系统服务运行的软件包。安装命令：

```sh
brew tap homebrew/services
```

使用 `brew services start` 启动服务，例如启动 `mysql`：

```sh
brew services start mysql
```

使用 `brew services stop` 停止服务：

```sh
brew services stop mysql
```

## **常用命令总结**
| 命令 | 作用 |
| --- | --- |
| brew search <软件包名> | 搜索软件包 |
| brew install <软件包名> | 安装软件包 |
| brew update | 更新 Homebrew 及软件包信息 |
| brew upgrade | 更新已安装的软件包 |
| brew uninstall <软件包名> | 卸载软件包 |
| brew list | 查看已安装的软件包 |
| brew info <软件包名> | 查看软件包信息 |
| brew services start <服务名> | 启动服务 |
| brew services stop <服务名> | 停止服务 |

## **参考资料**
[Homebrew 官网](https://brew.sh/)
[Homebrew GitHub 仓库](https://github.com/Homebrew/brew)
