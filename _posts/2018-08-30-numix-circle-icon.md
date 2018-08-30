---
layout: post
title: Numix Circle Icon Theme Fix for VS Code under Ubuntu
date:   2018-08-30 15:59:33
categories: linux
---

After installing the Visual Studio Code for Linux, I realized that my numix circle theme does not display correctly its icon (a file icon is displayed instead). Searching on the internet, I found this [solution](https://github.com/numixproject/numix-core/issues/2964) from the official numix repo. It appears that the default icon name "code" is too generic which may causes conflicts. There is no hardcore fix yet, but the numix team suggests copying and renaming the `/usr/share/applications/code.desktop` file to `~/.local/share/applications/vscode.desktop`, and replacing all `Icon=code` lines to `Icon=vscode`.

This would, however, create a duplicate of the icon. An alternative is to modify directly the `code.desktop` and then restart your session. The new `code.desktop` file will look like the following:
```
[Desktop Entry]
Name=Visual Studio Code
Comment=Code Editing. Redefined.
GenericName=Text Editor
Exec=/usr/share/code/code --unity-launch %F
Icon=vscode
Type=Application
StartupNotify=true
StartupWMClass=Code
Categories=Utility;TextEditor;Development;IDE;
MimeType=text/plain;inode/directory;
Actions=new-empty-window;
Keywords=vscode;

X-Desktop-File-Install-Version=0.22

[Desktop Action new-empty-window]
Name=New Empty Window
Exec=/usr/share/code/code --new-window %F
Icon=vscode
```
