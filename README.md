# DevOps System Setup:-

| <img src="Images/1-Banner.jpg"> |
| --------- |

| Windows System on which below application was Installed ? |
| --------- |
| Microsoft Windows Server 2022 Datacenter Azure Edition. |

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

3. __Install VSCODE on Windows.__

| Reference Link: https://community.chocolatey.org/packages/vscode |
| --------- |

```
choco install vscode
```

4. __Install GIT on Windows.__

| Reference Link: https://community.chocolatey.org/packages/vscode](https://community.chocolatey.org/packages/git.install |
| --------- |

```
choco install git.install
```

| Git Configuration after Installation:- |
| --------- |

```
git config --list
```

```
git config --global user.name "Arindam Mitra"
git config --global user.email mail2arindam2003@yahoo.com
git config --global init.defaultBranch main
```

```
git config --list
```

5. __Install PyCharm IDE (Community Edition) on Windows.__

| Reference Link: https://community.chocolatey.org/packages/pycharm-community |
| --------- |

```
choco install pycharm-community
```

6. __Install Terraform CLI on Windows.__

| Reference Link: https://winstall.app/apps/Hashicorp.Terraform |
| --------- |

```
winget install --id=Hashicorp.Terraform  -e --accept-source-agreements
```

| Terraform Installation Logs:- |
| --------- |

```
PS C:\Users\amadmin> winget install --id=Hashicorp.Terraform  -e --accept-source-agreements

The `msstore` source requires that you view the following agreements before using.
Terms of Transaction: https://aka.ms/microsoft-store-terms-of-transaction
The source requires the current machine's 2-letter geographic region to be sent to the backend service to function properly (ex. "US").

Found HashiCorp Terraform [Hashicorp.Terraform] Version 1.11.4
This application is licensed to you by its owner.
Microsoft is not responsible for, nor does it grant any licenses to, third-party packages.
Downloading https://releases.hashicorp.com/terraform/1.11.4/terraform_1.11.4_windows_amd64.zip
  ██████████████████████████████  26.8 MB / 26.8 MB
Successfully verified installer hash
Extracting archive...
Successfully extracted archive
Starting package install...
Command line alias added: "terraform"
Path environment variable modified; restart your shell to use the new value.
Successfully installed

PS C:\Users\amadmin>
```

7. __Install AzCLI Core on Windows.__

| Reference Link: https://community.chocolatey.org/packages/azure-cli |
| --------- |

```
choco install azure-cli -y
```

8. __Install Powershell Core on Windows.__

| Reference Link: https://winget.run/pkg/Microsoft/PowerShell |
| --------- |

```
winget install -e --id Microsoft.PowerShell
```

| Powershell Installation Logs:- |
| --------- |

```
PS C:\Users\amadmin> winget install -e --id Microsoft.PowerShell

Found PowerShell [Microsoft.PowerShell] Version 7.5.1.0
This application is licensed to you by its owner.
Microsoft is not responsible for, nor does it grant any licenses to, third-party packages.
Downloading https://github.com/PowerShell/PowerShell/releases/download/v7.5.1/PowerShell-7.5.1-win-x64.msi
  ██████████████████████████████   108 MB /  108 MB
Successfully verified installer hash
Starting package install...
Successfully installed

PS C:\Users\amadmin>
```
