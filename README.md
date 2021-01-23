# wsl


[https://cloud-images.ubuntu.com/releases/eoan/release/ubuntu-19.10-server-cloudimg-amd64-wsl.rootfs.tar.gz](https://cloud-images.ubuntu.com/releases/eoan/release/ubuntu-19.10-server-cloudimg-amd64-wsl.rootfs.tar.gz)

# Latest

[https://cloud-images.ubuntu.com/releases/server/bionic/release/ubuntu-18.04-server-cloudimg-amd64-wsl.rootfs.tar.gz](https://cloud-images.ubuntu.com/releases/server/bionic/release/ubuntu-18.04-server-cloudimg-amd64-wsl.rootfs.tar.gz)


# add the user via root
```bash
# as root
export NEWUSER=cicorias
adduser $NEWUSER
usermod -aG sudo $NEWUSER
```

# setting default user of a distro

```
$dname="ubuntu18.04A"
Get-ItemProperty Registry::HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Lxss\*\ DistributionName | Where-Object -Property DistributionName -eq $dnam  | Set-ItemProperty -Name DefaultUid -Value 1000
```

