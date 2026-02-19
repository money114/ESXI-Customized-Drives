# ESXI-Customized-Drives

ESXi 6.7封装第三方驱动    
-
1.下载VMware-PowerCLI-10.2.0-9372002    
2.在PowerShell中运行    
```
$env:PSModulePath
```
3.将VMware-PowerCLI-10.2.0-9372002文件复制到上述对应的目录    
4.下载最新ESXi6.7的zip文件    
5.下载6.7u3目录文件和ESXi-Customizer-PS.ps1    
6.将下载的ESXi和驱动文件放在同一目录    
7.PowerShell命令中将路径指向第4步的目录运行命令      
```
.\ESXi-Customizer-PS.ps1 -izip .\ESXi670-xxxxxxxxx.zip -pkgDir .\6.7u3 -nsc
```

ESXi 8.0封装第三方驱动    
-
1.以管理员权限运行Windows PowerShell安装最新版PowerCLI    
```
Install-Module -Name VMware.PowerCLI
```
2.安装Python 3.11    
3.下载get-pip.py    
4.安装get-pip.py    
```
<python3.11-directory>\python.exe <get-pip-directory>\get-pip.py
```
5.安装要求的Python模块    
```
<python3.11-directory>\Scripts\pip3.7.exe install six psutil lxml pyopenssl
```
6.在Powershell中配置Python3.11路径
```
Set-PowerCLIConfiguration -PythonPath <python3.11-directory>\python.exe -Scope User
```
7.下载最新ESXi8.0的zip文件    
8.下载8.0u3目录文件和ESXi-Customizer-PS.ps1    
9.将下载的ESXi和驱动文件放在同一目录    
10.PowerShell命令中将路径指向第11步的目录运行命令      
```
.\ESXi-Customizer-PS.ps1 -izip .\VMware-ESXi-8.0U3x-xxxxxxx-depot.zip -pkgDir .\8.0u3 -nsc
```
