

##wsl.conf

[automount]
enabled = true

[automount]
enabled = true
root = /mnt/

[automount]
enabled = true
mountFsTab = true
options = "metadata,umask=22,fmask=11"

[network]
generateHosts = true

[network]
generateHosts = true
generateResolvConf = true

[interop]
enabled = true

echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop

[interop]
enabled = true
appendWindowsPath = true

[user]
default = root

[boot]
command = apt update && apt upgrade -y

##.wslconfig


[wsl2]
kernel=C:\\Users\\Hayden\\bzImage
processors=4
memory=12GB
localhostforwarding=true
debugConsole=true
swap=6GB
swapfile=C:\\wslswap.vhdx
nestedVirtualization=true
debugConsole=true

Expose over LAN
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.1.100

