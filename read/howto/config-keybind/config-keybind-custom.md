---
title: 設定「自訂」的「按鍵綁定」
nav_order: 7020
has_children: false
parent: 設定「按鍵綁定 (Keybind)」
grand_parent: 如何
---


# 設定「自訂」的「按鍵綁定」




## 主題

* [前提](#前提)
* [設定範例](#設定範例)
* [範例腳本](#範例腳本)
* [相關案例](#相關案例)




## 前提




## 設定範例

``` sh

##
## ## Clear Old
##

dconf reset -f /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/




##
## ## Keybind Item
##


## ### Logout
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/name "'System_Logout'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/command "'gnome-session-quit --logout'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/binding "'<Shift><Alt>x'"


## ### Shutdown
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/name "'System_Shutdown'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/command "'gnome-session-quit --power-off'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/binding "'<Shift><Alt>z'"


## ### System Settings
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/name "'Control_Center'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/command "'gnome-control-center'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/binding "'<Shift><Alt>s'"


## ### Terminal
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/name "'Terminal'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/command "'gnome-terminal'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/binding "'<Alt>Return'"


## ### Terminal-1
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/name "'Terminal-1'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/command "'gnome-terminal'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/binding "'<Shift><Alt>a'"


## ### File Manager
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/name "'File_Manager'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/command "'nautilus'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/binding "'<Shift><Alt>f'"


## ### File Manager 1
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/name "'File_Manager-1'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/command "'thunar'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/binding "'<Shift><Alt>g'"


## ### Text Editor
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/name "'Text_Editor'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/command "'gnome-text-editor'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/binding "'<Shift><Alt>e'"


## ### Web Browser
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/name "'Web_Browser'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/command "'firefox --new-tab about:blank'"
dconf write /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/binding "'<Shift><Alt>b'"




##
## ## Custom Keybindings
##

gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings "['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/']"

```

> 上面設定完後，就會綁定成功。

> 可以執行下面指令，觀看目前的設定值。

``` sh

dconf dump /org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/

echo

gsettings get org.gnome.settings-daemon.plugins.media-keys custom-keybindings

```

顯示

```

[control-center]
binding='<Shift><Alt>s'
command='gnome-control-center'
name='Control_Center'

[file-manager-1]
binding='<Shift><Alt>g'
command='thunar'
name='File_Manager-1'

[file-manager]
binding='<Shift><Alt>f'
command='nautilus'
name='File_Manager'

[system-logout]
binding='<Shift><Alt>x'
command='gnome-session-quit --logout'
name='System_Logout'

[system-shutdown]
binding='<Shift><Alt>z'
command='gnome-session-quit --power-off'
name='System_Shutdown'

[terminal-1]
binding='<Shift><Alt>a'
command='gnome-terminal'
name='Terminal-1'

[terminal]
binding='<Alt>Return'
command='gnome-terminal'
name='Terminal'

[text-editor]
binding='<Shift><Alt>e'
command='gnome-text-editor'
name='Text_Editor'

[web-browser]
binding='<Shift><Alt>b'
command='firefox --new-tab about:blank'
name='Web_Browser'

['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-logout/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/system-shutdown/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/control-center/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/terminal-1/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/text-editor/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/web-browser/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/file-manager-1/']

```




## 範例腳本

* [範例腳本](https://github.com/samwhelp/note-about-ubuntu-gnome-shell/tree/gh-pages/_demo/scripts/gnome-shell-keybind)




## 相關案例

* [gnome-shell-keybind-custom](https://github.com/samwhelp/note-about-ubuntu/blob/gh-pages/_demo/adjustment/de/gnome-shell/part/gnome-shell-keybind-custom/config-install.sh)
* [/etc/dconf/db/distro.d/50_gnome-shell-keybind-custom.conf](https://github.com/samwhelp/lika-live-build-respin-gnome/blob/main/asset/overlay/etc/dconf/db/distro.d/50_gnome-shell-keybind-custom.conf)
