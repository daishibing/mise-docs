# Linux 安装配置

在 Linux 系统安装配置 mise

# 安装 mise

使用官方安装脚本安装 mise：

```shell
curl https://mise.run | sh
```

# 配置 Bash 自动激活 mise

将 mise 的 Bash 激活配置添加到 `~/.bashrc`：

```shell
echo 'eval "$(~/.local/bin/mise activate bash)"' >> ~/.bashrc
```

刷新当前终端配置：

```shell
source ~/.bashrc
```


