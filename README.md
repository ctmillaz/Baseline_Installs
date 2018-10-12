# Baseline_Installs

## NodeJS install

#### For Node.js v8 LTS
`curl --silent --location https://rpm.nodesource.com/setup_8.x | sudo bash -`

#### For Node.js v10 
`curl --silent --location https://rpm.nodesource.com/setup_10.x | sudo bash -`


#### Install
`sudo yum -y install nodejs`

#### Verify versions
`node -v`

`npm -v`

#### To install native addons from npm you need:
`sudo yum install gcc-c++ make`
#### or: sudo yum groupinstall 'Development Tools'

#### To install Yarn package manager run:
`curl -sL https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo`

#### To install Yarn
`sudo yum install yarn`

#### To uninstall
#### go to /usr/local/lib /usr/local/include /usr/local/bin and delete any node and node_modules
#### go to home directory and remove node and node_modules




--------------------------------------------------------------------------------------------------------------------------

## Visual Studio Install

#### Add stable x64 repo
`sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc`

`sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'`

#### Install Visual Code
`yum check-update`

`sudo yum install code`

#### Run Visual Code
#### Type this into command line:
`code`

#### Code needed to add Visual Studio to your desktop
`
[Desktop Entry]
Name=@@NAME_LONG@@
Comment=Code Editing. Redefined.
GenericName=Text Editor
Exec=/usr/share/@@NAME@@/@@NAME@@ --unity-launch %F
Icon=@@ICON@@
Type=Application
StartupNotify=true
StartupWMClass=@@NAME_SHORT@@
Categories=Utility;TextEditor;Development;IDE;
MimeType=text/plain;inode/directory;
Actions=new-empty-window;
Keywords=vscode;
`

`
[Desktop Action new-empty-window]
Name=New Empty Window
Exec=/usr/share/@@NAME@@/@@NAME@@ --new-window %F
Icon=@@ICON@@
`
