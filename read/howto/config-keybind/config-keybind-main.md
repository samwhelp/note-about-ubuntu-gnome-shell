---
title: 設定「主要」的「按鍵綁定」
nav_order: 7010
has_children: false
parent: 設定「按鍵綁定 (Keybind)」
grand_parent: 如何
---


# 設定「主要」的「按鍵綁定」




## 主題

* [前提](#前提)
* [設定範例](#設定範例)
* [統整](#統整)
* [範例腳本](#範例腳本)
* [相關案例](#相關案例)




## 前提

延續「[設定「按鍵綁定 (Keybind)」](https://samwhelp.github.io/note-about-ubuntu-gnome-shell/read/howto/config-keybind.html)」這篇找到的設定，

以下紀錄我常用的「視窗操作按鍵綁定」來當作「[設定範例](#設定範例)」說明。

> 要注意的是，以下只是單就個別項目做說明，有些綁定可能會跟目前既有的綁定衝突，所以要設定完整，還是要做統整的設定
以下紀錄並不全面。




## 設定範例

* [Window / Close](#window--close)
* [Window / Toggle Maximized](#window--toggle-maximized)
* [Window / Toggle Fullscreen](#window--toggle-fullscreen)
* [Window / Show Desktop](#window--show-desktop)
* [Window / Begin Move](#window--begin-move)
* [Window / Begin Resize](#window--begin-resize)
* [Alt-Tab Switcher](#alt-tab-switcher)
* [Window / Previous](#window--previous)
* [Window / Next](#window--next)
* [Workspace / Previous](#workspace--previous)
* [Workspace / Next](#workspace--next)
* [Overview / Show Apps](#overview--show-apps)
* [Overview / Scale](#overview--scale)
* [Window / Tiling Move](#window--tiling-move)
* [Screenshot](#screenshot)
* [統整](#統整)




## Window / Close

大部份的桌面環境，預設是綁定「`Alt + F4`」來「關閉視窗」。

```
org.gnome.desktop.wm.keybindings close ['<Alt>F4']
```

我個人慣用的是綁定「`Win + q`」來「關閉視窗」。


> 執行下面指令，綁定「`Win + q`」來「關閉視窗」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q']"
```


> 或是也可以執行下面指令，綁定「`Win + q`」來「關閉視窗」，並且也保留原來的「`Alt + F4`」綁定。

``` sh
gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q', '<Alt>F4']"
```

> 上面的範例，表示一個功能，可以有多重綁定。




## Window / Toggle Maximized

> 執行下面指令，綁定「`Win + w`」來「切換視窗最大化」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings toggle-maximized "['<Super>w']"
```




## Window / Toggle Fullscreen

> 執行下面指令，綁定「`Win + f`」來「切換視窗全螢幕」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings toggle-fullscreen "['<Super>f']"
```




## Window / Show Desktop

> 在「Ubuntu Gnome Shell」，預設就是綁定「`Win + d`」來「切換顯示桌面」。

```
org.gnome.desktop.wm.keybindings show-desktop ['<Primary><Super>d', '<Primary><Alt>d', '<Super>d']
```

> 執行下面指令，綁定「`Win + d`」來「切換顯示桌面」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings show-desktop "['<Super>d']"
```




## Window / Begin Move

> 執行下面指令，綁定「`Win + e`」來切換到「視窗開始移動」狀態。

``` sh
gsettings set org.gnome.desktop.wm.keybindings begin-move "['<Super>e']"
```




## Window / Begin Resize

> 執行下面指令，綁定「`Win + r`」來切換到「視窗開始更改大小」狀態。

``` sh
gsettings set org.gnome.desktop.wm.keybindings begin-resize "['<Super>r']"
```


> 關於「[begin-move](#window--begin-move)」和「[begin-resize](#window--begin-resize)」，可以對照另一篇『[設定「Mouse Button Modifier」](https://samwhelp.github.io/note-about-ubuntu-gnome-shell/read/howto/config-mouse-button-modifier.html)』提到的用法。




## Alt-Tab Switcher


## Window / Previous

> 執行下面指令，綁定「`Win + a`」來切換聚焦到「`上一個視窗`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-windows-backward "['<Super>a']"
```




## Window / Next

> 執行下面指令，綁定「`Win + s`」來切換聚焦到「`下一個視窗`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<Super>s']"
```




## Workspace / Previous

> 執行下面指令，綁定「`Alt + a`」來切換到「`上一個工作空間`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-left "['<Alt>a', '<Alt>Left']"
```




## Workspace / Next

> 執行下面指令，綁定「`Alt + s`」來切換到「`下一個工作空間`」。

``` sh
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-right "['<Alt>s', '<Alt>Right']"
```




## Overview / Show Apps

> 執行下面指令，綁定「`Win + grave`」來切換到「應用程式列表/所有工作空間概覽」。

``` sh
gsettings set org.gnome.shell.keybindings toggle-application-view "['<Super>grave', '<Super>Up']"
```

> 再按一次，則會切換到「[目前工作空間的所有視窗預覽/所有工作空間預覽](#overview--scale)」


> 在『[停用按鍵綁定「Super_L」開啟「Main Menu」](https://samwhelp.github.io/note-about-ubuntu-gnome-shell/read/howto/disable-keybind-open-main-menu.html#綁定衝突)』這篇有提到跟這個設定相關的綁定。




## Overview / Scale

> 執行下面指令，綁定「`Win + Tab`」來切換到「目前工作空間的所有視窗概覽/所有工作空間概覽」。

``` sh
gsettings set org.gnome.shell.keybindings toggle-overview "['<Super>Tab', '<Super>Down']"
```


| 方位        | 按鍵           | 功能                    |
| ----------- | -------------- | ----------------------- |
| 上 (Up)     | `Win + grave`  | `Overview / Show Apps`  |
| 下 (Down)   | `Win + Tab`    | `Overview / Scale`      |
| 左 (Left)   | `Alt + a`      | `Workspace / Previous`  |
| 右 (Right)  | `Alt + s`      | `Workspace / Next`      |
| 左 (Left)   | `Win + a`      | `Window / Previous`     |
| 右 (Right)  | `Win + s`      | `Window / Next`         |

> 關於「grave」指是「`」，在「Tab鍵」上方的那個「鍵盤按鍵」。

> `Win` for `Window`

> `Alt` for `Workspace`




## Window / Tiling Move

> 設定參考指令如下

``` sh

##
## ## Window / Tiling Move
##

gsettings set org.gnome.desktop.wm.keybindings maximize "['<Control><Super>Up']"

gsettings set org.gnome.desktop.wm.keybindings unmaximize "['<Control><Super>Down']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-left "['<Control><Super>Left']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-right "['<Control><Super>Right']"

```


## Screenshot

> 執行下面指令，探索關於「`screenshot`」的「按鍵綁定」設定

``` sh
gsettings list-recursively | grep screenshot
```

顯示

```
org.gnome.shell.keybindings screenshot ['<Shift>Print']
org.gnome.shell.keybindings screenshot-window ['<Alt>Print']
org.gnome.shell.keybindings show-screenshot-ui ['Print']
org.gnome.totem screenshot-save-uri ''
```


> 執行下面指令，修改關於「`screenshot`」的「按鍵綁定」設定

``` sh

##
## ## Screenshot
##

gsettings set org.gnome.shell.keybindings screenshot "['Print']"


##
## ## Screenshot / Window
##

gsettings set org.gnome.shell.keybindings screenshot-window "['<Super>Print']"


##
## ## Screenshot / Area
##

gsettings set org.gnome.shell.keybindings show-screenshot-ui "['<Alt>Print']"


##
## ## Screenshot / Recording
##

gsettings set org.gnome.shell.keybindings show-screen-recording-ui "['<Super>v']"

```

> `Super` for `Window`

> `Control` for `Area`




## 統整

> 統整以上提到的綁定

``` sh

##
## ## Fix
##


##
## ## Launcher
##

gsettings set org.gnome.desktop.wm.keybindings panel-main-menu "['<Alt>F1']"

gsettings set org.gnome.desktop.wm.keybindings panel-run-dialog "['<Alt>F2']"


##
## ## Window
##

gsettings set org.gnome.desktop.wm.keybindings close "['<Super>q']"

gsettings set org.gnome.desktop.wm.keybindings toggle-maximized "['<Super>w']"

gsettings set org.gnome.desktop.wm.keybindings toggle-fullscreen "['<Super>f']"

gsettings set org.gnome.desktop.wm.keybindings show-desktop "['<Super>d']"

gsettings set org.gnome.desktop.wm.keybindings begin-move "['<Super>e']"

gsettings set org.gnome.desktop.wm.keybindings begin-resize "['<Super>r']"


##
## ## Window / Switch
##

gsettings set org.gnome.desktop.wm.keybindings switch-windows-backward "['<Super>a']"

gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<Super>s']"

gsettings set org.gnome.desktop.wm.keybindings cycle-windows-backward "['<Alt>Escape', '<Super>Left']"

gsettings set org.gnome.desktop.wm.keybindings cycle-windows "['<Super>Escape', '<Super>Right']"


##
## ## Workspace / Switch
##

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-up "[]"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-down "[]"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-left "['<Alt>a', '<Alt>Left']"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-right "['<Alt>s', '<Alt>Right']"

gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-last "['<Alt>z']"


##
## ## Overview / Switch
##

gsettings set org.gnome.shell.keybindings toggle-application-view "['<Super>grave', '<Super>Up']"

gsettings set org.gnome.shell.keybindings toggle-overview "['<Super>Tab', '<Super>Down']"


##
## ## Window / Tiling Move
##

gsettings set org.gnome.desktop.wm.keybindings maximize "['<Control><Super>Up']"

gsettings set org.gnome.desktop.wm.keybindings unmaximize "['<Control><Super>Down']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-left "['<Control><Super>Left']"

gsettings set org.gnome.mutter.keybindings toggle-tiled-right "['<Control><Super>Right']"


##
## ## Screenshot
##

gsettings set org.gnome.shell.keybindings screenshot "['Print']"


##
## ## Screenshot / Window
##

gsettings set org.gnome.shell.keybindings screenshot-window "['<Super>Print']"


##
## ## Screenshot / Area
##

gsettings set org.gnome.shell.keybindings show-screenshot-ui "['<Alt>Print']"


##
## ## Screenshot / Recording
##

gsettings set org.gnome.shell.keybindings show-screen-recording-ui "['<Super>v']"

```


> 另外關於「Workspace」，我會做如下的額外設定


``` sh

gsettings set org.gnome.mutter dynamic-workspaces false

gsettings set org.gnome.desktop.wm.preferences num-workspaces 5

gsettings set org.gnome.desktop.wm.preferences workspace-names "['File', 'Edit', 'Web', 'Term', 'Misc']"

```




## 範例腳本

* [範例腳本](https://github.com/samwhelp/note-about-ubuntu-gnome-shell/tree/gh-pages/_demo/scripts/gnome-shell-keybind)




## 相關案例

* [gnome-shell-keybind-main](https://github.com/samwhelp/note-about-ubuntu/blob/gh-pages/_demo/adjustment/de/gnome-shell/part/gnome-shell-keybind-main/config-install.sh)
* [/usr/share/glib-2.0/schemas/50_gnome-shell-keybind-main.gschema.override](https://github.com/samwhelp/lika-live-build-respin-gnome/blob/main/asset/overlay/usr/share/glib-2.0/schemas/50_gnome-shell-keybind-main.gschema.override)
