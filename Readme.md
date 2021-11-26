# My Visual Studio Code Configuration and Extentions
I'm really attached to my setup in Visual Studio Code. And I want it to be in sync in any environment I work in.

________             ______             ________                           ______
___  __/___  ___________  /_______      ___  __ \_____ ___________________ ___  /
__  /  _  / / /_  ___/_  __ \  __ \     __  /_/ /  __ `/_  ___/  ___/  __ `/_  / 
_  /   / /_/ /_  /   _  /_/ / /_/ /     _  ____// /_/ /_(__  )/ /__ / /_/ /_  /  
/_/    \__,_/ /_/    /_.___/\____/      /_/     \__,_/ /____/ \___/ \__,_/ /_/   
                                                                                 
## Install Visual Studio Code
* Install Visual Studio Code [Visual Studio Code](https://code.visualstudio.com/download)

## Visual Studio Code Extentions
* Install the [REST Client extension](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) for Visual Studio Code

## CLI 
* Install Minikube to run Kubernetes locally [Minikube](https://minikube.sigs.k8s.io/docs/start/)
* Install Dapr CLI
```
wget -q https://raw.githubusercontent.com/dapr/cli/master/install/install.sh -O - | /bin/bash
```
* Install Chocolatey
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1’))
```
* Install Azure CLI
```
choco install azure-cli
```
* Install Gsudo (Easy Admin Priv switch in PowerShell) 
```
choco install gsudo
```
* Install Kubectl
```
choco install kubernetes-cli
```
* Install Curl (Optional: alternative for the Rest Client Extension)
```
choco install curl
```

# Terminal Interface
* Change execution policy
```
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
```
* Install [Oh-my-posh](https://ohmyposh.dev/)
Installation via choco
```
choco install oh-my-posh
```
```
Import-Module oh-my-posh
```
Edit $PROFILE
```
code . $PROFILE
```
Now you can make changes to your Profile settings, for example setting the theme
```ps1
Set-PoshPrompt -Theme https://github.com/pascalvanderheiden/my-visual-studio-code-setupturbopascal.omp.json
Set-PoshPrompt -Theme C:/github/my-visual-studio-code-setup/turbopascal.omp.json
```
Reload $PROFILE
```
. $PROFILE
```
Upgrade OhMyPosh
```
choco upgrade oh-my-posh
```
Fontfaces to use (Fonts are in this repo):
```json
"profiles": {
    "list": [
      {
        "fontFace": "CaskaydiaCove NF"
      }
    ]
}
```
```json
"profiles": {
    "list": [
      {
        "fontFace": "MesloLGM NF"
      }
    ]
}
```

* Install Posh-GIt
Install-Module posh-git -Scope CurrentUser -Force
Import-Module posh-git
Add-PoshGitToProfile -AllHosts