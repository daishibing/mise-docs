# Windows 安装配置

在 Windows 系统使用 PowerShell 安装配置 mise

# 安装 mise

使用 WinGet 安装 mise：

```shell
winget install jdx.mise
```

> 安装完成后，重启 PowerShell 使环境变量生效

# 配置 PowerShell 自动激活 mise

将 mise 的 PowerShell 激活配置添加到 `$PROFILE`：

```shell
if (-not (Test-Path $PROFILE)) {
    New-Item -ItemType Directory -Force (Split-Path -Parent $PROFILE) | Out-Null
    New-Item -ItemType File -Path $PROFILE | Out-Null
}
$activation = '(&mise activate pwsh) | Out-String | Invoke-Expression'
if (-not (Select-String -Path $PROFILE -SimpleMatch $activation -Quiet)) {
    Add-Content $PROFILE $activation
}
```

> 配置完成后，重启 PowerShell 使配置生效


