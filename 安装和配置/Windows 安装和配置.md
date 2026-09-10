# Windows 安装和配置

在 Windows 系统安装和配置 mise

# 安装 mise

使用 WinGet 安装 mise：

```shell
winget install jdx.mise
```

# 配置环境变量

将 mise 的 shims 添加到用户 `Path` 环境变量：

```text
%LOCALAPPDATA%\mise\shims
```

> 配置完成后，重新打开终端配置生效

# 查看 mise 版本

执行命令：

```shell
mise --version
```

# 检测 mise 完整性

执行命令：

```shell
mise doctor
```

输出中显示下面字样表示 mise 配置正常：

```text
No problems found
```


