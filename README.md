# DevOps System Setup:-

| Windows System on which below was Installed: Microsoft Windows Server 2022 Datacenter Azure Edition. |
| --------- |

1. __Install Chocolatey on Windows.__

| Reference Link: https://chocolatey.org/install |
| --------- |

```
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

| Validate Post Installation:- |
| --------- |

```
choco --version
```

2. __Install Winget on Windows.__

| Reference Link: https://learn.microsoft.com/en-us/windows/package-manager/winget/ |
| --------- |

```
Install-PackageProvider -Name NuGet -Force
Install-Module -Name Microsoft.WinGet.Client -Force -Repository PSGallery
Repair-WinGetPackageManager -AllUsers
```

| Validate Post Installation:- |
| --------- |

```
winget
```
