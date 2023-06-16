https://learn.microsoft.com/zh-cn/windows/wsl/install


```bash
wsl --install
```

## WSL不修改Windows主机名设置hostname的方法
https://blog.csdn.net/hxlawf/article/details/119750183
```bash
vim /etc/wsl.conf
[user]
default=robben

[network]
generateResolvConf=false
hostname=Ubuntu

# powershell
wsl --shutdown

```

## 修改用户名和密码
https://zhuanlan.zhihu.com/p/387283272

```bash
wsl.exe --user root

# 修改为root用户
passwd root
passwd username
```

win上不建议使用上述方法修改wsl的主机名，改了存在无法联网的风险


wsl methods to set proxy in wsl, adress: 
https://learn.microsoft.com/zh-cn/windows/wsl/networking


```bash
# methods

cat /etc/resolv.conf 

export https_proxy=xxx
export http_proxy=xxx

unset https_proxy
unset http_proxy


# 查看wsl安装位置 powershell
(Get-ChildItem -Path HKCU:\Software\Microsoft\Windows\CurrentVersion\Lxss | Where-Object { $_.GetValue(Ubuntu) -eq Ubuntu }).GetValue(BasePath) + "\ext4.vhdx"
```bash