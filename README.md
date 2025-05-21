# DevOps System Setup:-

| <img src="Images/1-Banner.jpg"> |
| --------- |

| Windows System on which below application was Installed ? |
| --------- |
| Microsoft Windows Server 2022 Datacenter Azure Edition. |

| List of Application Name Installed ? |
| --------- |
| 1. Chocolatey. |
| 2. Winget. |
| 3. VSCode. |
| 4. Git. |
| 5. Pycharm IDE. |
| 6. Terraform CLI. |
| 7. AzCLI. |
| 8. Powershell Core. |
| 9. Google Chrome. |
| 10. Kubectl. |
| 11. Kubeadmin. |
| 12. Helm. |

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

🔥 Important Note: __Refer to the Github Link where I have raised issue - https://github.com/asheroto/winget-install/issues/64__ 

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
| __Reference Link: https://git-scm.com/book/ms/v2/Getting-Started-First-Time-Git-Setup__ |

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

🔥 Important Note: __Refer to the Github Link where I have raised issue - https://github.com/microsoft/winget-pkgs/issues/259029__

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

9. __Install Google Chrome on Windows.__

| Reference Link: https://community.chocolatey.org/packages/GoogleChrome |
| --------- |

🔥 Important Note: __Click on the above Link, Scroll down and refer to the comment Section. I have updated all below details there as well.__

```
choco install googlechrome
```

| Google Chrome ERROR Installation Logs:- |
| --------- |

```
PS C:\Users\amadmin> choco install googlechrome

Chocolatey v2.4.3
Installing the following packages:
googlechrome
By installing, you accept licenses for the packages.
Downloading package from source 'https://community.chocolatey.org/api/v2/'
Progress: Downloading GoogleChrome 135.0.7049.96... 100%

GoogleChrome v135.0.7049.96 [Approved]
GoogleChrome package files install completed. Performing other installation steps.
The package GoogleChrome wants to run 'chocolateyInstall.ps1'.
Note: If you don't run this script, the installation will fail.
Note: To confirm automatically next time, use '-y' or consider:
choco feature enable -n allowGlobalConfirmation
Do you want to run the script?([Y]es/[A]ll - yes to all/[N]o/[P]rint): A

Downloading googlechrome 64 bit
  from 'https://dl.google.com/dl/chrome/install/googlechromestandaloneenterprise64.msi'
Progress: 100% - Completed download of C:\Users\amadmin\AppData\Local\Temp\chocolatey\GoogleChrome\135.0.7049.96\googlechromestandaloneenterprise64.msi (128.07 MB).
Download of googlechromestandaloneenterprise64.msi (128.07 MB) completed.
Error - hashes do not match. Actual value was '3DA6536F05FC2121310CFD768F168BD759DE5CDC69F1D05DD14A1B6A67370250'.
ERROR: Checksum for 'C:\Users\amadmin\AppData\Local\Temp\chocolatey\GoogleChrome\135.0.7049.96\googlechromestandaloneenterprise64.msi' did not meet '020d946e9d3be75242f672830f6b6dd335d49aa34e5030864690e539b579f176' for checksum type 'sha256'. Consider passing the actual checksums through with --checksum --checksum64 once you validate the checksums are appropriate. A less secure option is to pass --ignore-checksums if necessary.
The install of GoogleChrome was NOT successful.
Error while running 'C:\ProgramData\chocolatey\lib\GoogleChrome\tools\chocolateyInstall.ps1'.
 See log for details.

Chocolatey installed 0/1 packages. 1 packages failed.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).

Failures
 - GoogleChrome (exited -1) - Error while running 'C:\ProgramData\chocolatey\lib\GoogleChrome\tools\chocolateyInstall.ps1'.
 See log for details.

PS C:\Users\amadmin>
```

| Correct Command:- |
| --------- |

```
choco install googlechrome -y --ignore-checksums
```

10. __Install Kubectl on Windows.__

| Reference Link: https://community.chocolatey.org/packages/kubernetes-cli |
| --------- |

```
choco install kubernetes-cli
```

| Kubectl Installation Logs:- |
| --------- |

```
PS C:\Users\amadmin> choco install kubernetes-cli

Chocolatey v2.4.3
Installing the following packages:
kubernetes-cli
By installing, you accept licenses for the packages.
Downloading package from source 'https://community.chocolatey.org/api/v2/'
Progress: Downloading kubernetes-cli 1.33.0... 100%

kubernetes-cli v1.33.0 [Approved]
kubernetes-cli package files install completed. Performing other installation steps.
The package kubernetes-cli wants to run 'chocolateyInstall.ps1'.
Note: If you don't run this script, the installation will fail.
Note: To confirm automatically next time, use '-y' or consider:
choco feature enable -n allowGlobalConfirmation
Do you want to run the script?([Y]es/[A]ll - yes to all/[N]o/[P]rint): A

Extracting 64-bit C:\ProgramData\chocolatey\lib\kubernetes-cli\tools\kubernetes-client-windows-amd64.tar.gz to C:\ProgramData\chocolatey\lib\kubernetes-cli\tools...
C:\ProgramData\chocolatey\lib\kubernetes-cli\tools
Extracting 64-bit C:\ProgramData\chocolatey\lib\kubernetes-cli\tools\kubernetes-client-windows-amd64.tar to C:\ProgramData\chocolatey\lib\kubernetes-cli\tools...
C:\ProgramData\chocolatey\lib\kubernetes-cli\tools
 ShimGen has successfully created a shim for kubectl-convert.exe
 ShimGen has successfully created a shim for kubectl.exe
 The install of kubernetes-cli was successful.
  Deployed to 'C:\ProgramData\chocolatey\lib\kubernetes-cli\tools'

Chocolatey installed 1/1 packages.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).

PS C:\Users\amadmin>

```

| Validate Post Installation:- |
| --------- |

```
PS C:\Users\amadmin> kubectl version --client
Client Version: v1.33.0
Kustomize Version: v5.6.0
PS C:\Users\amadmin>
```

11. __Install kubelogin on Windows.__

| Reference Link: https://community.chocolatey.org/packages/kubelogin  |
| --------- |

🔥 Important Note: __Refer to the below chocolatey community, Stackoverflow & Github Link where I have provided my solution on the issue encountered.__

- https://community.chocolatey.org/packages/kubelogin

- https://stackoverflow.com/questions/74702519/executable-kubelogin-failed-with-exit-code-1/79626355#79626355
 
- https://github.com/Azure/kubelogin/issues/544

- https://github.com/Azure/kubelogin/issues/139

- https://github.com/lensapp/lens/issues/7956

```
choco install kubelogin
```

| Kubelogin Installation Logs:- |
| --------- |

```
PS C:\Users\amadmin> choco install kubelogin
Chocolatey v2.4.3
Installing the following packages:
kubelogin
By installing, you accept licenses for the packages.
Downloading package from source 'https://community.chocolatey.org/api/v2/'
Progress: Downloading kubelogin 1.32.4... 100%

kubelogin v1.32.4 [Approved]
kubelogin package files install completed. Performing other installation steps.
The package kubelogin wants to run 'chocolateyInstall.ps1'.
Note: If you don't run this script, the installation will fail.
Note: To confirm automatically next time, use '-y' or consider:
choco feature enable -n allowGlobalConfirmation
Do you want to run the script?([Y]es/[A]ll - yes to all/[N]o/[P]rint): A

Extracting 64-bit C:\ProgramData\chocolatey\lib\kubelogin\tools\kubelogin_windows_amd64.zip to C:\ProgramData\chocolatey\lib\kubelogin\tools...
C:\ProgramData\chocolatey\lib\kubelogin\tools
Added C:\ProgramData\chocolatey\bin\kubectl-oidc_login.exe shim pointed to '..\lib\kubelogin\tools\kubelogin.exe'.
 ShimGen has successfully created a shim for kubelogin.exe
 The install of kubelogin was successful.
  Deployed to 'C:\ProgramData\chocolatey\lib\kubelogin\tools'

Chocolatey installed 1/1 packages.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).
PS C:\Users\amadmin>
```


| Kubelogin ERROR Logs:- |
| --------- |

__AKS uses kubelogin plugin for authentication.__

> kubelogin convert-kubeconfig -l azurecli
```
PS C:\Users\amadmin> kubelogin convert-kubeconfig -l azurecli
error: unknown shorthand flag: 'l' in -l
```

| Troubleshooting:- |
| --------- |

Uninstall kubelogin using choco.
> choco uninstall kubelogin -y
```
PS C:\Users\amadmin> choco uninstall kubelogin -y
Chocolatey v2.4.3
Uninstalling the following packages:
kubelogin

kubelogin v1.32.4
Removing shim C:\ProgramData\chocolatey\bin\kubectl-oidc_login.exe which pointed to ''.
 Skipping auto uninstaller - No registry snapshot.
 kubelogin has been successfully uninstalled.

Chocolatey uninstalled 1/1 packages.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).
PS C:\Users\amadmin>
```

__Install kubelogin using Azure Github: https://azure.github.io/kubelogin/install.html__

> winget install --id=Microsoft.Azure.Kubelogin  -e

```
PS C:\Users\amadmin> winget install --id=Microsoft.Azure.Kubelogin  -e
Found Microsoft Azure Kubelogin [Microsoft.Azure.Kubelogin] Version 0.2.8
This application is licensed to you by its owner.
Microsoft is not responsible for, nor does it grant any licenses to, third-party packages.
Downloading https://github.com/Azure/kubelogin/releases/download/v0.2.8/kubelogin-win-amd64.zip
  ██████████████████████████████  23.4 MB / 23.4 MB
Successfully verified installer hash
Extracting archive...
Successfully extracted archive
Starting package install...
Command line alias added: "kubelogin"
Successfully installed
PS C:\Users\amadmin>
```

| Validate Post Installation:- |
| --------- |

> kubelogin --version
```
PS C:\Users\amadmin> kubelogin --version
kubelogin version
git hash: v0.2.8/d7f1c16c95cc0a1a3beb056374def7b744a38b3a
Go version: go1.23.7
Build time: 2025-04-25T17:17:57Z
Platform: windows/amd64
PS C:\Users\amadmin>
```

__Get Credentials:-__

> az aks get-credentials --resource-group AM-CrossPlane-RG --name AM-Crossplane-AKS --overwrite-existing

```
PS C:\Users\amadmin> az aks get-credentials --resource-group AM-CrossPlane-RG --name AM-Crossplane-AKS --overwrite-existing
Merged "AM-Crossplane-AKS" as current context in C:\Users\amadmin\.kube\config
PS C:\Users\amadmin>
```

__Use kubelogin plugin for authentication:-__

> kubelogin convert-kubeconfig -l azurecli
```
PS C:\Users\amadmin> kubelogin convert-kubeconfig -l azurecli
PS C:\Users\amadmin>
```

> kubectl get nodes
```
PS C:\Users\amadmin> kubectl get nodes
NAME                                STATUS   ROLES    AGE    VERSION
aks-agentpool-99335204-vmss000000   Ready    <none>   3h7m   v1.31.7
PS C:\Users\amadmin>
```

12. __Install Helm on Windows.__

| Reference Link: https://community.chocolatey.org/packages/kubernetes-helm |
| --------- |

```
choco install kubernetes-helm
```

| Kubectl Installation Logs:- |
| --------- |

```
PS C:\Users\amadmin> choco install kubernetes-helm
Chocolatey v2.4.3
Installing the following packages:
kubernetes-helm
By installing, you accept licenses for the packages.
Downloading package from source 'https://community.chocolatey.org/api/v2/'
Progress: Downloading kubernetes-helm 3.17.3... 100%

kubernetes-helm v3.17.3 [Approved]
kubernetes-helm package files install completed. Performing other installation steps.
The package kubernetes-helm wants to run 'chocolateyInstall.ps1'.
Note: If you don't run this script, the installation will fail.
Note: To confirm automatically next time, use '-y' or consider:
choco feature enable -n allowGlobalConfirmation
Do you want to run the script?([Y]es/[A]ll - yes to all/[N]o/[P]rint): A

Downloading kubernetes-helm 64 bit
  from 'https://get.helm.sh/helm-v3.17.3-windows-amd64.zip'
Progress: 100% - Completed download of C:\Users\amadmin\AppData\Local\Temp\2\chocolatey\kubernetes-helm\3.17.3\helm-v3.17.3-windows-amd64.zip (17.09 MB).
Download of helm-v3.17.3-windows-amd64.zip (17.09 MB) completed.
Hashes match.
Extracting C:\Users\amadmin\AppData\Local\Temp\2\chocolatey\kubernetes-helm\3.17.3\helm-v3.17.3-windows-amd64.zip to C:\ProgramData\chocolatey\lib\kubernetes-helm\tools...
C:\ProgramData\chocolatey\lib\kubernetes-helm\tools
 ShimGen has successfully created a shim for helm.exe
 The install of kubernetes-helm was successful.
  Deployed to 'C:\ProgramData\chocolatey\lib\kubernetes-helm\tools'

Chocolatey installed 1/1 packages.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).
PS C:\Users\amadmin>
PS C:\Users\amadmin>

```

| Validate Post Installation:- |
| --------- |

```
PS C:\Users\amadmin> helm version
version.BuildInfo{Version:"v3.17.3", GitCommit:"e4da49785aa6e6ee2b86efd5dd9e43400318262b", GitTreeState:"clean", GoVersion:"go1.23.7"}
PS C:\Users\amadmin>
```


