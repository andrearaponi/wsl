
**Checking update
wsl --version
wsl --update

**Listing all distro

wsl -l
wsl --list
wsl --list --running
wsl -l -v


**Running a specific distro

wsl -d distroname
wsl -d distroname -u user

**Terminate a distro

wsl -t distroname
wsl --terminate distroname

**Shutdown all distro

wsl --shutdown

**Run a single command with wsl

wsl --exec echo 'hello Eng!'
wsl -d distroname --exec cat /etc/os-release
wsl -d distroname --user root --exec whoami

**Setting a default distro

wsl -s distroname
wsl --set-default distroname

**Converting distro between wsl versions

wsl --set-version nomedistro 1

**Export/Import

wsl --export distroname C:\WSL\distroname-backup.tar.gz
wsl --import distroname C:\installationpath C:\backuplocation --version 2


**Mounting a partitioned disk

GET-CimInstance -query "SELECT * from Win32_DiskDrive"
wsl --mount <DiskPath> --bare
wsl --unmount <DiskPath>