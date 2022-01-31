# Windows10-11-CreationScript-Feb2022
Use this ansible script to install software, create users, and update your Windows 10/11 System. 

# Enable WinRM on Remote Machine using this Action Script
```
$url = "https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1"
$file = "$env:temp\ConfigureRemotingForAnsible.ps1"
(New-Object -TypeName System.Net.WebClient).DownloadFile($url, $file)
powershell.exe -ExecutionPolicy ByPass -File $file
winrm enumerate winrm/config/Listener
```
# To run the script, use the following command:
```
sudo ansible-playbook win-create.yml -i hosts
```
