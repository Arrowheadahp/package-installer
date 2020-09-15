FOR WINGET INSTALL:

search for app installer in windows app store and update it.
Then run the .appxbundle


then run the following command

for /f "tokens=*" %a in (packages.txt) do winget install %a --force







FOR CHOCO INSTALL:

run the following command in admin cmd to install choco
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command " [System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

copy the packages.txt to C drive and run the following command in admin cmd

for /f "tokens=*" %a in (../../packages.txt) do choco install %a -y
