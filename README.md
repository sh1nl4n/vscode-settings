## Install from archive

[Download Visual Studio Code] (https://code.visualstudio.com/Download)

```bash
sudo tar -xzf ~/Downloads/code-stable-x64-1683731267.tar.gz -C /opt/
sudo ln -s /opt/VSCode-linux-x64/bin/code /usr/local/bin/code
sudo vim /usr/share/applications/code.desktop
```

### File code.desktop

```
[Desktop Entry]
Name=Visual Studio Code
GenericName=Text Editor. Refined.
Comment=Code Editing, Redefined
Exec=/usr/local/bin/code --unity-launch %F
Icon=/opt/VSCode-linux-x64/resources/app/resources/linux/code.png
Type=Application
StartupWMClass=Code
StartupNotify=true
Categories=TextEditor;Development;IDE;
MimeType=text/plain;inode/directory;application/x-code-workspace;
Actions=new-empty-window;
Keywords=vscode;


[Desktop Action new-empty-window]
Name=New Empty Window
Exec=/usr/local/bin/code --new-window %F
Icon=/opt/VSCode-linux-x64/resources/app/resources/linux/code.png
```

### code-url-handler.desktop

```
[Desktop Entry]
Name=Visual Studio Code - URL Handler
Comment=Code Editing. Redefined.
GenericName=Text Editor
Exec=/usr/local/bin/code --open-url %U
Icon=/opt/VSCode-linux-x64/resources/app/resources/linux/code.png
Type=Application
NoDisplay=true
StartupNotify=true
Categories=TextEditor;Development;IDE;
MimeType=x-scheme-handler/vscode;
```

## Install config

```
sudo mkdir /usr/share/fonts/VsCode/
sudo cp ~/Downloads/visual-studio-code-config/fonts/* /usr/share/fonts/VsCode/
sudo fc-cache -f -v
```

- copy code from setting.json file to User JSON
